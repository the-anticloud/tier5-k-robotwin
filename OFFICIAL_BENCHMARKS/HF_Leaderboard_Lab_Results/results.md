# HF_Leaderboard_Lab_Results

**Project:** `K_ROBOTWIN`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `RoboTwin-Platform/RoboTwin`  
**Commit:** `ea8b21121ebb`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **56.39 ms** |
| Min latency | 51.97 ms |
| Max latency | 63.03 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **35** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5855 |
| Classification latency | 115.51 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_ROBOTWIN (RoboTwin-Platform/RoboTwin) — 753 files, 23900 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'robot', '##win', '(', 'robot', '##win', '-', 'platform', '/', 'robot', '##win', ')', '—', '75', '##3', 'files', ',', '239']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_