# Radon_Complexity_Lab_Results
**Project:** `K_DEEPSEEKHARN` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `2`
- **average_complexity:** `{'grade': 'A', 'score': 4.176470588235294}`
- **complexity_grade:** `A`
- **complexity_score:** `4.176470588235294`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_DEEPSEEKHARN\UPSTREAM\verify_urls.py - A (40.44)
E:\fenta\Dow`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_DEEPSEEKHARN\UPSTREAM\verify_urls.py
    F 164:0 print_summary - C (13)
    M 112:4 URLValidator.check_one - C (11)
    M 94:4 URLValidator.split_urls - B (7)
    F 201:0 main - B (6)
    C 48:0 URLValidator - B (6)
    M 72:4 URLValidator.load_cache - A (4)
    M 60:4 URLValidator.extract_urls - A (3)
    M 147:4 URLValidator.check_all - A (3)
    F 192:0 save_json - A (2)
    C 30:0 URLStatus - A (1)
    C 39:0 URLResult - A (1)
    M 49:4 URLValidator.__init__ - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_DEEPSEEKHARN\UPSTREAM\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)

17 blocks (classes, functions, methods) analyzed.
Average complexity: A (4.176470588235294)
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_