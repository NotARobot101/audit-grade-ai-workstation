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
- A receipt bundle as a **folder** 

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


