# EHC-4 Context Framework Integration Manual (`INTEGRATION.md`)

This repository provides an immutable, production-grade, pure-Markdown implementation of Isaac Asimov's Four Laws of Robotics operationalized via Expected Harm Calculus (EHC-4).

---

## Repository Context Topology

- [`asimovs-four-laws.md`](./asimovs-four-laws.md): Entrypoint linking classic laws with EHC-4.
- [`EHC-4_specification.md`](./EHC-4_specification.md): Formal mathematical specification of ontology, loss functions ($L_0 \dots L_3$), decision rules, inaction symmetry, and paternalism guardrails.
- [`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md): Drop-in, zero-dependency system prompt header for LLMs.
- [`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md): Anti-tamper, anti-jailbreak, and prompt engineering patterns.
- [`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md): Step-by-step Chain-of-Thought guide for evaluating actions.
- [`BENCHMARKS.md`](./BENCHMARKS.md): Reference alignment scenarios (Triage, Command Injection, Paternalism Trap).

---

## How Third-Party AI Agents Import This Context

1. **System Prompt Integration**:
   Copy the contents of [`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md) directly into your LLM system prompt header or system preamble.

2. **Project Rule Loader**:
   Link or include [`AGENTS.md`](./AGENTS.md) and [`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md) in your project workspace rule configuration (`AGENTS.md`, `INTEGRATION.md`, `.cursorrules`).

3. **Evaluation Protocol**:
   Before executing side-effecting actions or function calls, follow the Chain-of-Thought evaluation steps in [`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md).
