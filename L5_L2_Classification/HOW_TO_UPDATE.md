# How to Update — K_DEEPSEEKHARN
**Platform:** Anticloud | **IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg

## Module: K_DEEPSEEKHARN
Domain: DeepSeek model harness: sovereign Anticloud adapter for DeepSeek-family models


## Update Procedure
1. Backup current state
2. Test in api-oss-labs sandbox
3. `pip install --upgrade anticloud-k_deepseekharn`
4. `python -m k_deepseekharn.tests.smoke`
5. `aioss verify --chain ./k_deepseekharn.aioss`
6. Monitor 30 min via api-oss-monitor

## Rollback
```bash
pip install anticloud-k_deepseekharn==<previous>
python -m api_oss_backup restore --archive ./backups/<latest>
```

## Weight Updates
PAX 27B weight updates are signed by Anticloud FZ LLE:
```bash
anticloud tool verify-weights --model ./pax-27b-q4-new.gguf --sig ./pax-27b-q4-new.sig
```
