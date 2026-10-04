# Ledger Status

**Project:** `K_ROBOTWIN`  
**Tier:** TIER_5_WORLD_NEURO_EMBODIED  
**Identity:** Upstream `RoboTwin-Platform/RoboTwin` @ `ea8b21121ebb` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `RoboTwin-Platform/RoboTwin` |
| Commit | `ea8b21121ebb3cd201ff5b3fe361944ac94eda3f` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 7.21 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
