# Deploy Guide — K_ROBOTWIN
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, K_HELIX (physics), PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, K_HELIX physics engine, ROS2 (for data collection), PAX 27B.

## Environment
T4 GPU for policy training. K_HELIX physics requires CUDA. ROS2 for demonstration recording.

## AIOSS Integration
```bash
aioss init --module K_ROBOTWIN --output ./k_robotwin.aioss
aioss append --chain ./k_robotwin.aioss --payload ./output.bin --module K_ROBOTWIN
aioss verify --chain ./k_robotwin.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_ROBOTWIN",
    aioss_chain="./K_ROBOTWIN.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_ROBOTWIN.aioss --verbose
python -m K_ROBOTWIN.tests.smoke
```
