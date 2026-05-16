# ADR-ABADIA-20260515-002: Monastic Connection (MCP Server Spec)

> **Standard:** AHE-ADR-v1
> **Level:** System / Infrastructure
> **Owner:** [[hermes-agent]] / juantomas garcia

---

## Metadata
```yaml
adr_id: ADR-ABADIA-20260515-002
title: "Implementation of an MCP Server as the Game Harness Bridge"
date: 2026-05-15
status: Proposed
scope: Infrastructure
tags: [mcp, infrastructure, harness, connectivity]
transcript_ref: "Session 2026-05-15 (Infrastructure Planning)"
```

---

## 1. Context and Problem Statement
abadIA needs a way for autonomous agents (Hermes, Claude, etc.) to interact with the game microservice. The current microservice provides a REST API. Directly calling REST endpoints lacks the standard discovery and typing required for seamless multi-agent orchestration.

## 2. Decision Drivers
1. **Interoperability:** Any MCP-compliant agent should be able to play the game.
2. **Deterministic Inputs:** Tool calling via MCP is more reliable than raw HTTP requests for agents.
3. **Abstraction:** The agent should see "Actions" (e.g., `move_to(location)`) rather than URLs.

## 3. Decision Outcome
**Selected:** Develop a **Model Context Protocol (MCP) Server** that wraps the existing REST microservice.

### 4.1. Tool Specification (Initial)
The MCP Server will expose the following tools:
- `get_game_state()`: Returns the full 100% semantic JSON.
- `execute_action(action_id)`: Sends input to the game (up, down, left, right, examine, pick_up).
- `get_map_context()`: Returns semantic info about current coordinates.

---

## 5. Harness Rules (Machine-Readable Constraints)
> **CRITICAL:** These rules apply to the implementation of the MCP bridge.

- **Rule 1:** Every REST response must be mapped to a typed JSON schema in the MCP output.
- **Rule 2:** The MCP server must provide a `hint` field in the state to guide agentic "next steps" during the early learning phase.
- **Rule 3:** Maximum latency for MCP-REST roundtrip: 500ms.

---

## 6. Verification Proof
- **Computational:** [Pending implementation]
- **Inferential:** [Draft approved by User]

---
*Created via [[hub-daily-pulse]] | Managed by [[harness-standard-v3]]*
