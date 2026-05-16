# Chapter: The Osmani Cycle in Practice

To build a sovereign system like **AbadIA**, we don't just "write code." We orchestrate a deterministic loop. Following the **Osmani Standard**, every change follows this 4-stage process harness.

## 1. The Skill: `osmani-standard-workflow`

This skill is the "Constitutional Guard" of the project. It is activated automatically when the agent reads the `AGENTS.md` file.

### Stage 1: SPEC (The Contract)
Before any action, we define the **Spec**. 
- **Tool:** `agentic-spec-management`.
- **Requirement:** A modular file in `docs/specs/` (< 200 lines).
- **Mandatory:** A "Verification & Validation" section. If you can't test it, you can't spec it.

### Stage 2: PLAN (The Spec-to-Task Loop)
We transform the Spec into a series of atomic tasks.
- **Rule:** Each task must be executable in a single agent turn (< 50 lines of change).
- **Tool:** `writing-plans`.

### Stage 3: BUILD (The Beyoncé Rule)
We implement the logic.
- **Principle:** "If you liked it, you shoulda put a test on it." 
- **Action:** Write the test in `tests/` first. Ensure it fails (Red). Then build until it passes (Green).

### Stage 4: VERIFY (Proof of Sovereignty)
The task is not done until the command output is visible in the session log.
- **Evidence:** Terminal output showing 100% test success.

## 2. Why this matters?
This cycle prevents **"Context Rot"** and **"Vibe Coding"**. It ensures that if the human (the Master) leaves, the agent (the Novice) has everything it needs to maintain the system's integrity.

---
*Standard: [[harness-standard-v3]] | Managed by [[addy-osmani]]*
