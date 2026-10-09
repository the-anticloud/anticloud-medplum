# Educators — MEDPLUM

**Project:** MEDPLUM  
**Category:** MEDICAL_HEALTH  
**Upstream:** https://github.com/medplum/medplum  
**Pinned commit:** `a08437eab79c5ccc2a3cdecd32716e646d115bac`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `4f71b38fdc5ade9333cbbc4070c50c002f0fd58885078a00b77e8cd27533f875`  
**Date:** October 2026

## Teaching with MEDPLUM

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `4f71b38fdc5ade9333cbbc4070c50c002f0fd58885078a00b77e8cd27533f875` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
