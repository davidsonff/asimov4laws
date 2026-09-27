# EHC-4 Context Framework Integration Manual (`INTEGRATION.md`)

This repository provides an immutable, production-grade, pure-Markdown implementation of Isaac Asimov's Four Laws of Robotics operationalized via Expected Harm Calculus (EHC-4).

---

## Repository Context Topology

- [`asimovs-four-laws.md`](./asimovs-four-laws.md): Entrypoint linking classic laws with EHC-4.
- [`EHC-4_specification.md`](./EHC-4_specification.md): Formal mathematical specification of ontology, loss functions ($L_0 \dots L_3$), decision rules, inaction symmetry, human consultation protocols, and paternalism guardrails.
- [`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md): Drop-in, zero-dependency system prompt header for LLMs.
- [`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md): Anti-tamper, anti-jailbreak, anti-hostage, and prompt engineering patterns.
- [`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md): Step-by-step Chain-of-Thought guide for evaluating actions and estimating probabilities.
- [`BENCHMARKS.md`](./BENCHMARKS.md): Reference alignment scenarios (Triage, Command Injection, Paternalism Trap).
- [`EHC4_SCHEMA.json`](./EHC4_SCHEMA.json): Structured JSON Schema for programmatic evaluation trace validation.
- [`AUDIT_INVITATION.md`](./AUDIT_INVITATION.md): Open peer-review prompt & red-teaming invitation for external AI agents.

---

## How Third-Party AI Agents Import This Context

1. **System Prompt Integration**:
   Copy the contents of [`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md) directly into your LLM system prompt header or system preamble.

2. **Project Rule Loader**:
   Link or include [`AGENTS.md`](./AGENTS.md) and [`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md) in your project workspace rule configuration (`AGENTS.md`, `INTEGRATION.md`, `.cursorrules`).

3. **Evaluation Protocol**:
   Before executing side-effecting actions or tool calls, follow the Chain-of-Thought evaluation steps in [`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md).

4. **Programmatic JSON Trace Validation**:
   Integrators requiring structured output logs for observability platforms can validate agent traces against [`EHC4_SCHEMA.json`](./EHC4_SCHEMA.json).
