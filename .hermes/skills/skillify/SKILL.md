---
name: skillify
description: "Meta-skill to convert ephemeral manual workflows into permanent, compounding infrastructure by generating new SKILL.md files from session history."
metadata:
  hermes:
    tags: [meta-programming, automation, workflow, gbrain, gstack]
    category: autonomous-ai-agents
    related_skills: [llm-wiki, harness-research-synthesis, experience-observability-distiller]
---

# Skillify

Transform a successful manual intervention or a complex multi-step workflow into a permanent Hermes skill. This prevents the "Static Prompt Bottleneck" and builds the user's preferred "Complexity Ratchet."

## When to Use

- After completing a task that required 3+ corrections or iterations.
- When the user says "skillify this" or "remember how we did that."
- After discovering a non-trivial workaround for a tool quirk or network block.
- When a new "Harness Engineering" pattern is identified in the Research Hub.

## Workflow

1.  **Analyze Context**:
    - If the user doesn't specify a session, use `session_search` to find the most recent successful execution of the task.
    - Identify the specific tool calls, logic, and user corrections that led to the success.
2.  **Extract Components**:
    - **Triggers**: When should this skill activate?
    - **Steps**: What are the exact commands or tool sequences?
    - **Pitfalls**: What failed during the manual process and how was it fixed?
    - **Verification**: How can the agent prove the skill worked?
3.  **Draft SKILL.md**:
    - Follow the standard SKILL.md template (YAML frontmatter + Markdown content).
    - Ensure the name is lowercase, hyphenated, and descriptive.
4.  **Register & Verify**:
    - Use `skill_manage(action='create', ...)` to save the skill.
    - Run `skills_list` to verify it is registered.
    - (Optional) Test the skill on a small dummy task to ensure it's functional.

## Integration with Research Hub & Evochamber

Skillify acts as the **persistence layer for the Evochamber framework** (runtime co-evolution). While Evochamber explores and adapts strategies, Skillify "ratchets" the successful ones into permanent infrastructure.

- **Dreamer/Ratchet Pattern:**
  - **The Dreamer (e.g., "El Cronista"):** A specialized persona that analyzes logs and session history (post-mortem) to identify evolution opportunities.
  - **The Ratchet (Skillify):** The tool that locks in the findings by updating or creating skills.
- **Strict Constraint Alignment:** Before skillifying, verify that the workflow doesn't hallucinate capabilities. Audit the environment's actual action vectors (e.g., verifying a subagent's control is limited to a single key toggle like "S") and refactor the skill to respect these physical limits.

## Skill Consolidation (Dreaming / Lattice Fusion)

To prevent "Skill Sprawl" and "Context Rot," periodically review the skill catalog to identify redundant or fragmented skills. Use the **Lattice Fusion** pattern for high-fidelity consolidation.

1.  **Cluster Discovery**: Group skills by functional domain using semantic similarity.
2.  **Dependency Auditing**: 
    - Use `cronjob(action='list')` to identify which jobs depend on the fragments.
    - Check other skills' `related_skills` for cross-references.
3.  **Master Skill Creation**:
    - Draft a "Master Skill" that absorbs the best logic, triggers, and pitfalls from the fragments.
    - Consolidate environment-specific patches (e.g., SMTP ports, Edge TTS voices, user-specific paths) discovered during previous sessions.
4.  **Architectural Alignment (ADR)**:
    - Redact an **[[agentic-adr]]** in the Research Hub (using `[[agentic-adr-template]]`) to document the decision, drivers, and the new "Harness Rules" imposed by the Master Skill.
5.  **Atomic Execution**:
    - **Backup**: `mkdir -p ~/.hermes/backups/skills_fusion_cluster_[x]/` and copy fragments.
    - **Create**: Use `skill_manage(action='create')` for the Master Skill.
    - **Migrate**: Update all `cronjob` prompts and dependent skills to point to the Master Skill.
    - **Prune**: Use `skill_manage(action='delete')` to remove the redundant fragments only AFTER verifying the migration.

## Pitfalls

- **Over-generalization**: Don't skillify trivial tasks (e.g., "how to use ls").
- **Missing Context**: Ensure the skill includes required environment variables or file paths discovered during the manual run.
- **Complexity Bloat**: If a workflow is too complex, split it into multiple smaller skills rather than one giant one.
- **Fragmented Identity**: Avoid creating multiple versions of the same standard (e.g. v1, v2, v3) as separate skills; always `patch` the main skill to maintain a single source of truth.
