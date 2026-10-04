# Deploy Guide — K_DEEPSEEKHARN
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, PyTorch 2.10+, transformers 4.40+, DeepSeek weights, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, transformers 4.40+, DeepSeek weights (download separately, verify checksums).

## Environment
24GB+ VRAM for DeepSeek-V2. CPU inference for smaller DeepSeek variants. 32GB RAM.

## AIOSS Integration
```bash
aioss init --module K_DEEPSEEKHARN --output ./k_deepseekharn.aioss
aioss append --chain ./k_deepseekharn.aioss --payload ./output.bin --module K_DEEPSEEKHARN
aioss verify --chain ./k_deepseekharn.aioss
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
    module="K_DEEPSEEKHARN",
    aioss_chain="./K_DEEPSEEKHARN.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_DEEPSEEKHARN.aioss --verbose
python -m K_DEEPSEEKHARN.tests.smoke
```
