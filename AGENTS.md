# AGENTS.md — abadIA Autonomous Operations Manual (HE v3.0)

This is the canonical source of truth for all autonomous agents (Gemini-cli, Antigravity/Honcho, Claude Code, Hermes) operating on the abadIA project.

## 1. Agnostic Sovereignty
abadIA does not depend on a specific model's flavor. We design for **Agent-First Engineering**, where the Harness governs the Model.

## 2. Operating Standards (HE v3.0)
All agents must adhere to the **Osmani Standard (Spec-Plan-Build-Verify)** and the 7-step deterministic cycle:
1. **Declaration:** Identify yourself and state your assumptions before acting.
2. **Contracting:** Create/update `SPEC.md` or a Service-Level ADR in `docs/adr/`.
3. **The Beyoncé Rule:** Tests in `tests/` MUST exist and FAIL before logic is implemented.
4. **Agent Legibility Gate:** 
   - Files must be < 200 lines. 
   - Use modular, self-documenting code (Atoms/Molecules).
   - Refactor if complexity exceeds agentic context efficiency.

## 3. Toolchain & Interaction
- **Primary Harness:** `ralph-loop.sh` (The Ralph Loop).
- **Primary Interface:** `gemini-cli` + `antigravity`.
- **Memory:** `antigravity` (Honcho) captures the "Dreamer" state.
- **Skills:** This repository contains local skills in `.hermes/skills/`. Agents MUST load these skills (e.g., using `skill_view`) to handle project-specific workflows.
- **Verification:** `pytest` + `ruff`.

## 4. The Ralph Loop (The Ratchet)
The Ralph Loop is the primary execution engine for long, unattended tasks.
- **Workflow:** Fresh session per iteration -> State lives in `plan/plan.md` and `plan/task/NN.md`.
- **Stop Signal:** Creation of `stop.md` (manual or agentic).
- **Commands:**
  - `/ralph set-up`: Initialize the plan structure.
  - `/ralph fase0`: Decompose plan into actionable tasks.

## 5. Atomic Teaching Protocol
No task is "Done" until the educational artifacts are generated:
- **Log:** Update `docs/wiki/log.md`.
- **Teaching:** New concept in `docs/wiki/concepts/`.
- **Production:** New pack in `docs/production/`.

## 6. Visual Standards
Use the Lattice Visual System (Cyan/Emerald/Violet) for all architecture assets.

---
*Identity: Agent-Native | Standard: HE v3.0 | Engine: Ralph*