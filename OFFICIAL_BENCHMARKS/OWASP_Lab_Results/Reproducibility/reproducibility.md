# Reproducibility Record: OWASP_Lab_Results

**Project:** `K_ROBOTWIN`  
**Benchmark:** `OWASP_Lab_Results`  
**Run:** `2026-09-30T15:11:19.033679+00:00`  
**Based on:** [HELM reproducibility principles](https://github.com/stanford-crfm/helm)

## Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| OS | `nt` |

## Inputs

| Field | Value |
| ----- | ----- |
| Slug | `RoboTwin-Platform/RoboTwin` |
| Commit | `ea8b21121ebb` |
| Tracked files | `753` |
| Source lines | `23900` |
| Licence | `MIT` |
| Inputs SHA256 | `066a62ea76bb495c...` |

## Outputs

| Field | Value |
| ----- | ----- |
| Results file | `TIER_5_WORLD_NEURO_EMBODIED\K_ROBOTWIN\OFFICIAL_BENCHMARKS\OWASP_Lab_Results\results.json` |
| Results SHA256 | `560dca14b7f013d2...` |

## Reproduction Steps

- 1. Clone Anticloud at commit HEAD
- 2. Ensure E:\fenta\Downloads\The Anticloud is present
- 3. Run: python run_benchmarks_comprehensive.py
- 4. Run: python write_benchmark_subfolders.py
- 5. Run: python write_ledgers_repro_extra_benchmarks.py
- 6. Verify results_sha256 matches sha256(OFFICIAL_BENCHMARKS/OWASP_Lab_Results/results.json)

## Notes

TRL/OSINT/OWASP/SOC2/ISO27001/MITRE/NIST use static code analysis. HF uses live CPU inference.

---
_Anticloud Reproducibility Standard v1 — 2026-09-30T15:11:19.033679+00:00_