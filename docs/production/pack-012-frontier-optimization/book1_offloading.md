# Chapter: Offloading Reasoning to Local Primitives

In **HE v3.0**, we distinguish between "Strategic Reasoning" (LLM) and "Reflexive Validation" (Local Skills). This chapter explains how we optimize the agent's frontier by moving mechanical tasks out of the inference loop.

## 1. The Token Tax
Every time an agent asks the LLM "Can I move to 134,170?", it pays a tax in latency and tokens. For a 2x2 grid check, this is unacceptable.

## 2. Local Skills as Habits
We implement **Local Habits** using Python scripts:
- **`abadia-logic-validator`**: Replaces LLM spatial guessing with a deterministic geometric check.
- **`chronicler-parser`**: Replaces LLM log reading with high-speed regex/jq filtering.
- **`monastic-sensor-trigger`**: Replaces LLM deliberation with hard-coded interrupts for bells and orders.

## 3. The Result
By offloading these tasks, the agent's context window stays clean for high-level mystery solving, while the local harness handles the "monastic reflexes."

---
*Pack: 012 | Standard: [[harness-standard-v3]]*
