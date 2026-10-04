# Ledger Status

**Project:** `K_DEEPSEEKHARN`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `ai-boost/awesome-harness-engineering` @ `7df8f81c2128` (CC0-1.0)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `ai-boost/awesome-harness-engineering` |
| Commit | `7df8f81c2128cd23a675bf9771113b558008d348` |
| Upstream licence | CC0-1.0 |
| Licence class | permissive |
| Clone size | 0.43 MB |
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
