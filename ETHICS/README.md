# Ethics — MEDPLUM

**Project:** MEDPLUM  
**Category:** MEDICAL_HEALTH  
**Upstream:** https://github.com/medplum/medplum  
**Pinned commit:** `a08437eab79c5ccc2a3cdecd32716e646d115bac`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `4f71b38fdc5ade9333cbbc4070c50c002f0fd58885078a00b77e8cd27533f875`  
**Date:** October 2026

## Position

MEDPLUM is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
