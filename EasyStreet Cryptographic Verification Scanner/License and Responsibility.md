This tool verifies cryptographic integrity only. It does not provide legal, compliance, or operational advice.
Use is at your own risk. Decisions recorded in receipt bundles remain the responsibility of their Operators.


---

```md
# README_VERIFY.md

# Verify a Receipt Bundle (30 seconds)

This tool verifies cryptographic integrity only.  
It does not evaluate, approve, endorse, or interpret decisions.

## 1) What you need
- Python 3 installed (no internet required)
- A receipt bundle as a **folder** or a **ZIP**

The bundle must include:
- `Decision_Receipt.md`
- `MANIFEST.json`
- `TEST_INDEX.csv`
- `trace.jsonl`
- `ROOT.txt`

## 2) Run verification

### Folder
```bash
python inspector.py ./receipt_bundle

ZIP
python inspector.py ./receipt_bundle.zip

3) Read the result

The verifier prints a terminal status and writes:

INSPECTION_REPORT.md

inspection_result.json

Exit codes:

0 = VALID (cryptographic integrity intact)

1 = INVALID (seal broken / mismatch detected)

2 = MALFORMED (missing/unsupported/incomplete bundle)

4) What VALID means (and does not mean)

VALID means:

The cryptographic seal matches the artifacts as provided.

Any tampering would have been detected.

VALID does NOT mean:

The underlying decision was correct, safe, compliant, or lawful.

The evidence was complete or accurate.

This tool reports math, not judgment.


---

```md
# SECURITY.md

# Security Policy

## Scope
This repository provides a read-only, offline verifier for receipt bundles.

The scanner:
- does not execute receipt contents,
- does not fetch external resources,
- does not modify bundles,
- does not provide compliance or remediation guidance.

## Reporting issues
If you find a verification bypass, parsing ambiguity, or integrity weakness:
- Open an issue with a minimal reproducible bundle (redacted)
- Include expected vs actual exit codes and the failing invariant
- Do NOT include sensitive customer data, secrets, or private evidence

## Non-goals
This project is not a vulnerability research submission channel and does not accept reports that require:
- network access,
- privileged environment assumptions,
- exploit payload distribution.
