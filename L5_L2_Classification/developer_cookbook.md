# Developer Cookbook — K_DEEPSEEKHARN
**Stack:** Python 3.11, PyTorch 2.10+, transformers 4.40+, DeepSeek weights, AIOSS_FORMAT
**Domain:** DeepSeek model harness: sovereign Anticloud adapter for DeepSeek-family models

## Load DeepSeek via Anticloud harness
```python
from k_deepseekharn import DeepSeekHarness

harness = DeepSeekHarness(
    model="deepseek-coder-33b-instruct",
    weights_path="./deepseek-coder-33b/",
    aioss_chain="./deepseekharn.aioss"
)
result = harness.generate(
    prompt="Write a Python function to append entries to an AIOSS chain",
    max_tokens=512, temperature=0.1
)
print(result.text, result.chain_hash)
```

## Route between PAX 27B and DeepSeek
```python
from pax_router import PAXRouter
router = PAXRouter(
    default_model="pax-27b",
    routing_rules={"coding": "deepseek-coder", "math": "deepseek-math"}
)
result = router.infer("Write a CUDA kernel for Flash Attention")
```

## Benchmark vs PAX 27B
```python
bench = harness.compare_with_pax(
    pax_model="./pax-27b-q4.gguf",
    benchmark="anticloud_coding_bench"
)
print(f"DeepSeek: {bench.deepseek_score:.2f} | PAX: {bench.pax_score:.2f}")
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
