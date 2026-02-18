# docs/INVARIANTS.md

# Verification Invariants (Fail-Closed)

These invariants define the verifier’s behavior. Breaking any invariant is a hard failure.

## Invariant 1 — Read-only truth
The verifier cannot mutate receipt state.
No repairs, normalization, “helpful fixes,” or rewriting.

## Invariant 2 — No judgment
The verifier reports integrity state only.
No risk scoring, compliance opinions, or operational conclusions.

## Invariant 3 — Binary machine truth
Cryptographic layer yields only:
- VALID (0)
- INVALID (1)
- MALFORMED (2)

No warnings. No partial credit.

## Invariant 4 — Explanation is not advice
Human-readable output translates mechanical facts only.
No remediation instructions.

## Invariant 5 — Strict version pinning
Unknown or ambiguous versions are refused.

## Invariant 6 — Air-gapped verification
No internet required. No external lookups.
If verification requires external data → fail.

## Invariant 7 — Mandatory disclaimer
Every report must state:
“This tool verifies cryptographic integrity only. It does not evaluate, approve, endorse, or interpret decisions.”

## Invariant 8 — Evidence over intent
No inference about why a decision was made or whether tampering was malicious.
Only “what failed, where, and how.”
