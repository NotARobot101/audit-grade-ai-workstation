# Decision Receipt (Example)

Receipt ID: EXAMPLE-RCPT-0001  
Receipt Version: 1.0 (Frozen)  
Generation Time (UTC): YYYY-MM-DD HH:MM:SS UTC  

---

## 1. Decision Summary

Decision Recorded: Example — Full Test Suite Execution  
Decision Type: Operational / Deployment Authorization  
Outcome: Approved and Executed  

This receipt records who approved what, when, and with what evidence.  
It does not evaluate correctness, safety, legality, or regulatory compliance.

---

## 2. Evidence Bound to the Decision

The following evidence items were bound to this decision at the time of authorization.
Each item is represented by a cryptographic hash.

- 01_INTERFACE_COMPATIBILITY — SHA256(EXAMPLE_REDACTED)
- 02_PIPELINE_EXECUTION_LOGS — SHA256(EXAMPLE_REDACTED)
- 03_PRE_DEPLOYMENT_FREEZE — SHA256(EXAMPLE_REDACTED)
- 04_POST_DEPLOYMENT_SNAPSHOT — SHA256(EXAMPLE_REDACTED)
- 05_DEPENDENCY_RISK_REVIEW — SHA256(EXAMPLE_REDACTED)
- 06_SECRETS_HANDLING_AUDIT — SHA256(EXAMPLE_REDACTED)
- 07_VENDOR_INTEGRATION_REVIEW — SHA256(EXAMPLE_REDACTED)
- 08_REGULATORY_READINESS_CHECK — SHA256(EXAMPLE_REDACTED)

Evidence was supplied by the Operator.  
EasyStreet does not verify the accuracy or completeness of evidence.

---

## 3. Human Authorization (Causal Control)

Authorized Role: Operational Lead  
Authorization Method: Identity-Locked Digital Signature  
Authorization Time (UTC): YYYY-MM-DD HH:MM:SS UTC  

Execution was cryptographically blocked until all required authorizations were present.

---

## 4. Cryptographic Seal (Illustrative)

Seal Construction (conceptual):

H(Evidence_Hashes || Authorized_Identities || Decision_Metadata || Timestamp)

Root Hash: SHA256(EXAMPLE_REDACTED)

Verification Properties:
- Deterministic
- Tamper-evident
- Reproducible

Note: This example omits machine-verifiable artifacts.

---

## 5. Scope & Disclaimers

This receipt records a decision.  
It does not approve, validate, or endorse the decision.

All legal, regulatory, and operational responsibility remains with the Operator.

Any modification to evidence, identities, or timing invalidates the seal.

---

## 6. Verification (Conceptual)

In a live deployment, verification consists of:
1. Recomputing hashes for all evidence items
2. Verifying identity signatures
3. Recalculating the root hash
4. Confirming an exact match

Verification tooling and full artifacts are generated per engagement and are not published.
