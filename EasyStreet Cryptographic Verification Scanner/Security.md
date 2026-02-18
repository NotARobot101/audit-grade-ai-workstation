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
