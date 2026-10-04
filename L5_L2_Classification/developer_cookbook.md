# Developer Cookbook — K_ROBOTWIN
**Stack:** Python 3.11, PyTorch 2.10+, K_HELIX (physics), PAX 27B, AIOSS_FORMAT
**Domain:** RoboTwin: twin-based robot learning from demonstration with physics validation

## Record and learn from demonstration
```python
from k_robotwin import RoboTwinLearner

learner = RoboTwinLearner(
    robot_urdf="./robot.urdf",
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./robotwin.aioss"
)

# Validate demonstration in physics twin
demo = learner.load_demonstration("./demo_pick_place.bag")
validation = learner.validate_in_twin(demo)
print(f"Physics valid: {validation.valid}, collisions: {validation.n_collisions}")

# Train policy
if validation.valid:
    policy = learner.train(demo, n_epochs=100)
    print(f"Policy success rate: {policy.validation_success_rate:.2%}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
