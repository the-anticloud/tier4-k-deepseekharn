# L5 Narrow / L2 General Classification — K_DEEPSEEKHARN
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_DEEPSEEKHARN wraps DeepSeek-V2/Coder/Math inference in the Anticloud PAX harness protocol: AIOSS chain append, air-gap operation, MF_SO_PASSWORD_MANAGER for weight keys. It does not modify model architecture — only the integration layer.

## L2 General
L2 General: TIER_4 inference agents route coding tasks to DeepSeek-Coder and math tasks to DeepSeek-Math through the same harness interface as PAX 27B. PAX_ROUTER handles the dispatch transparently.

## PAX 27B Integration
PAX 27B and DeepSeek models work in ensemble: PAX handles general Anticloud queries, K_DEEPSEEKHARN routes specialized coding/math tasks to DeepSeek. PAX_ROUTER (TIER_2) makes the routing decision.

## AIOSS Audit Chain
Every inference result (model version hash + prompt hash + completion hash + routing metadata) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
ISO/IEC 42001 (AI system documentation). No external regulatory for inference adapters.
