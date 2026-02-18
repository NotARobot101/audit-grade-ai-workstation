
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
