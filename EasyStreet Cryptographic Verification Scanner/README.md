# README.md

# EasyStreet Cryptographic Verification Scanner

A read-only, offline tool that mechanically verifies the cryptographic integrity of sealed EasyStreet receipt bundles.

**This tool verifies cryptographic integrity only. It does not evaluate, approve, endorse, or interpret decisions.**

## What it does
Given a sealed receipt bundle (folder or ZIP), the scanner performs deterministic verification:
- Recomputes SHA-256 for bound evidence/components
- Verifies internal consistency across `MANIFEST.json`, `TEST_INDEX.csv`, and `trace.jsonl`
- Verifies the hash-chain integrity of `trace.jsonl`
- Verifies the final commitment in `ROOT.txt`
- Enforces strict version pinning (e.g., `Receipt Version: 1.0 (Frozen)`)

## What it does NOT do
- No “risk scoring” or compliance grading
- No remediation advice
- No workflow integration, API calls, or network activity
- No receipt generation, editing, repairing, or normalization
- No inference of intent, fault, or legal conclusions

## Inputs (receipt bundle requirements)
A valid bundle must include:
- `Decision_Receipt.md`
- `MANIFEST.json`
- `TEST_INDEX.csv`
- `trace.jsonl`
- `ROOT.txt`

The scanner is fail-closed. Missing or malformed artifacts result in a non-zero exit code.

## Outputs
The scanner produces:
- `INSPECTION_REPORT.md` (human-readable mechanical translation)
- `inspection_result.json` (machine-readable summary)

Exit codes:
- `0` = VALID (cryptographic integrity intact)
- `1` = INVALID (integrity broken / mismatch detected)
- `2` = MALFORMED (missing/unsupported/incomplete bundle)

## Quick start

### Verify a folder bundle
```bash
python inspector.py /path/to/receipt_bundle

