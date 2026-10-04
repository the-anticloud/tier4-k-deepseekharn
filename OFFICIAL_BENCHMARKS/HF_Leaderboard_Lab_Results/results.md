# HF_Leaderboard_Lab_Results

**Project:** `K_DEEPSEEKHARN`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `ai-boost/awesome-harness-engineering`  
**Commit:** `7df8f81c2128`  
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
| Avg latency | **53.31 ms** |
| Min latency | 45.07 ms |
| Max latency | 61.57 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **42** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5786 |
| Classification latency | 94.97 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_DEEPSEEKHARN (ai-boost/awesome-harness-engineering) — 12 files, 245 source lines, licence CC0-1.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'deep', '##see', '##khar', '##n', '(', 'ai', '-', 'boost', '/', 'awesome', '-', 'harness', '-', 'engineering', ')', '—', '12']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_