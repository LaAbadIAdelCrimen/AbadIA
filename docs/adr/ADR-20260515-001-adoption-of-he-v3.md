# ADR-ABADIA-20260515-001: Adoption of Harness Engineering (HE) v3.0

> **Standard:** AHE-ADR-v1
> **Level:** Service / Project
> **Owner:** [[hermes-agent]] / juantomas garcia

---

## Metadata
```yaml
adr_id: ADR-ABADIA-20260515-001
title: "Adoption of HE v3.0 as the Core Methodology"
date: 2026-05-15
status: Accepted
scope: Repository
tags: [methodology, he-v3, transition, education]
transcript_ref: "Session 2026-05-15 (Initialization)"
```

---

## 1. Context and Problem Statement
abadIA is currently a project built primarily via "Vibe Coding" (exploratory, non-deterministic interaction). To scale it and ensure maintainability—while simultaneously serving as a master template for other projects—it needs to be refactored into a structured, verifiable, and deterministic system using the latest standards of Harness Engineering.

## 2. Decision Drivers
1. **Verifiability:** Move from "it seems to work" to "it is proven to work via sensors."
2. **Didactic Potential:** Every change must serve as a teaching moment for the community.
3. **Agent Legibility:** Ensure future agents can maintain the project with minimal context rot.
4. **Repeatability:** Create a template that can be applied to other projects in the user's ecosystem.

## 3. Decision Outcome
**Selected:** Full adoption of **Harness Engineering (HE) v3.0**.

**Justification:** HE v3.0 provides the rigorous 7-step loop (/spec to /distill) and the "Beyoncé Rule" (no code without tests) required for high-quality agéntic development.

---

## 4. Harness Rules (The Contract)
1. **Spec-First:** No implementation in `src/` without an approved `SPEC.md`.
2. **Beyoncé Rule:** Every vertical slice must have an associated test in `tests/`.
3. **Atomic Teaching:** Every step must generate an educational artifact in `docs/production/`.
4. **Dual-Wiki Linkage:** Decisions here must link back to theoretical concepts in the central Research Hub (`~/wiki`).

---

## 5. Verification Proof
- **Computational:** Repository structure and Wiki initialization confirmed.
- **Inferential:** User-approved initialization of the "abadIA Genome."
