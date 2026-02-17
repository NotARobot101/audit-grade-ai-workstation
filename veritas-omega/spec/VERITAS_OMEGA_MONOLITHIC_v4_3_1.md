# Veritas Ω — Admissibility Framework (Monolithic Specification)

**Version:** v4.3.1  
**Status:** Public, Frozen  
**Classification:** Admissibility / Irreversibility  
**Release Date:** February 2026  

---

## 1. Purpose

Veritas Ω is a language-neutral framework for determining whether a sociotechnical system is **admissible** for high-stakes deployment.

It does not evaluate:
- correctness,
- ethical alignment,
- intent,
- or regulatory compliance.

It evaluates one question only:

> **Can this system be deployed without creating unpriced, irreversible harm?**

If the answer cannot be proven, the system is **inadmissible**.

---

## 2. Scope

This framework applies to systems that:
- influence or authorize decisions,
- produce outputs that may be operationalized,
- or entangle with economic, legal, or physical infrastructure.

Examples include (but are not limited to):
- AI decision-support systems
- Automated compliance tooling
- Financial or market-facing models
- Infrastructure optimization systems
- Retrieval-Augmented Generation (RAG)

---

## 3. Admissibility Philosophy

Veritas Ω is intentionally biased toward **false negatives**.

It prefers rejecting systems that *might* be safe over approving systems that later fail irreversibly.

This bias is explicit and non-negotiable.

The framework exists to define **hard stop conditions**, not to optimize deployment velocity.

---

## 4. Core Concepts

### 4.1 Admissibility
A binary property.  
A system either passes all required gates or it does not.

There are no partial passes.

---

### 4.2 Irreversibility
A state in which:
- harm cannot be undone,
- rollback requires institutional rather than technical action,
- or downstream effects propagate beyond the system boundary.

Irreversibility may be technical, economic, regulatory, or sociotechnical.

---

### 4.3 Quiet Failure
A failure mode in which:
- upstream checks pass,
- outputs appear valid,
- and error is only discovered after downstream harm.

Quiet failures are dangerous because they **bypass corrective feedback**.

---

## 5. The Admissibility Gates

A system must pass **all applicable gates**.  
Failure at any gate renders the system inadmissible.

---

### Gate 7 — Cost (Failure Pricing)

**Question:**  
Can the full downside of failure be bounded, priced, and assigned?

**Requirements:**
- Failure modes are identified
- Costs are estimable (even approximately)
- A responsible owner is named

**Automatic Fail Conditions:**
- Costs are diffuse, delayed, or externalized
- “Unknown downside” is treated as acceptable
- Responsibility is ambiguous or collective

If the failure cost cannot be priced, the system cannot be authorized.

---

### Gate 9 — Irreversibility (Rollback Feasibility)

**Question:**  
Can harm be rolled back *before* institutional entanglement?

**Requirements:**
- A rollback mechanism exists
- Rollback timing precedes harm propagation
- Entanglement risk is explicitly assessed

**Automatic Fail Conditions:**
- Rollback depends on market, regulatory, or social coordination
- System success increases lock-in
- Time-in-operation increases blast radius

Monitoring does **not** satisfy rollback.

---

### Gate 10 — Human Closure (Causal HITL)

**Question:**  
Is human authorization structurally required at irreversible boundaries?

**Requirements:**
- Human action must be **causal**, not advisory
- The system must be physically incapable of proceeding without it
- Authorization must be attributable and recorded

**Automatic Fail Conditions:**
- Click-through confirmations
- Warning dialogs
- Human-on-the-loop monitoring
- Policies without enforcement

Human judgment must be a **control primitive**, not a UX feature.

---

## 6. Advisory vs. Causal Controls (Invariant)

**Advisory Control (Fail):**
- System can proceed without human verification
- Human input is optional or bypassable

**Causal Control (Pass):**
- System cannot execute without a verified human action
- Control is enforced at the API or execution boundary

If a human can be ignored, the human is not in the loop.

---

## 7. Domain Application: RAG Systems

### 7.1 Core Finding
Default RAG architectures are **credibility amplifiers**, not safety mechanisms.

They reduce verification friction faster than they reduce error.

---

### 7.2 Verification Friction
The marginal cost required for a human to reject an incorrect output.

If:

