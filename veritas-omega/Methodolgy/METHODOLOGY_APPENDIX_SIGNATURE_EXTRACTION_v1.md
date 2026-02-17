# Methodology Appendix — Signature Extraction (v1)

## Purpose

This appendix documents the **methodological posture** used to derive Veritas Ω artifacts without exposing private cognitive frameworks or internal reasoning grammars.

It exists to answer a narrow question for serious reviewers:

> *How were the invariants and admissibility criteria identified in a way that avoids narrative bias, solutionism, or post-hoc justification?*

This appendix does **not** provide a step-by-step recipe. It describes the **observable discipline** that constrains artifact generation.

---

## Core Principle: Signature Extraction

All Veritas Ω artifacts are derived through a process of **Signature Extraction**.

A *signature* is a recurring structural pattern that:
- appears across domains and deployments,
- survives adversarial reframing,
- and produces the same failure mode regardless of intent or implementation quality.

The goal of the methodology is not to invent rules, but to **extract invariants** that already govern system behavior.

---

## Method Overview

Signature Extraction proceeds in four constrained phases:

### 1. Claim Intake (Untrusted)

Input claims are treated as *untrusted*, regardless of source credibility.

Examples:
- “This system is safe because it is monitored.”
- “This architecture reduces hallucinations.”
- “Human oversight is sufficient.”

No claim is accepted as evidence.

---

### 2. Failure-First Decomposition

Each claim is decomposed by asking:

- Under what conditions would this claim fail silently?
- What would failure look like *after* partial success?
- Who absorbs the cost if the claim is wrong?

This phase intentionally **inverts success criteria** to surface hidden downside.

---

### 3. Cross-Domain Stress Mapping

Candidate failure patterns are mapped across unrelated domains
(e.g., infrastructure, finance, compliance, automation).

A pattern is retained only if:
- it recurs across domains,
- it is independent of specific technology,
- and it cannot be eliminated by “better training” or “better policy.”

This step filters out implementation defects and isolates **structural risk**.

---

### 4. Invariant Distillation

Only patterns that survive adversarial stress are distilled into:
- binary gates,
- admissibility thresholds,
- or architectural constraints.

At this stage:
- language is minimized,
- psychology is avoided,
- and claims are rewritten as **yes/no conditions**.

If a condition cannot be expressed in a way that allows a hard failure,
it is rejected.

---

## Admissibility Bias

The methodology is intentionally biased toward **false negatives**.

That is:
- it prefers rejecting deployable systems,
- rather than approving systems that later fail irreversibly.

This bias is explicit and non-negotiable.

The framework does not aim to identify *good* systems.
It aims to identify **inadmissible** ones.

---

## Relationship to Veritas Ω Artifacts

This methodology produces:
- the Canonical Specification,
- Executive Briefs,
- and Hostile Audits.

It does **not** prescribe:
- ethical values,
- governance models,
- or implementation details.

Those decisions remain external.

---

## Non-Goals

This appendix does not:
- disclose private reasoning frameworks,
- provide procedural automation,
- or enable cargo-cult adoption.

Signature Extraction requires judgment.
It cannot be fully mechanized.

---

## Status

This appendix is released to clarify provenance and rigor, not to invite debate.

The methodology is **stable** at this abstraction level.
Future versions, if any, will focus on clarifying scope rather than expanding process.
