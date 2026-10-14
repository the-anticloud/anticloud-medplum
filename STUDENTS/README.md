# Students — MEDPLUM

**Project:** MEDPLUM  
**Category:** MEDICAL_HEALTH  
**Upstream:** https://github.com/medplum/medplum  
**Pinned commit:** `a08437eab79c5ccc2a3cdecd32716e646d115bac`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `4f71b38fdc5ade9333cbbc4070c50c002f0fd58885078a00b77e8cd27533f875`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `a08437eab79c5ccc2a3cdecd32716e646d115bac`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `4f71b38fdc5ade9333cbbc4070c50c002f0fd58885078a00b77e8cd27533f875`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
