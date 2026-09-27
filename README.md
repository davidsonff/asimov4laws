# Expected Harm Calculus (EHC-4): Asimov's Four Laws for Autonomous AI Agents

[![Pure Markdown](https://img.shields.io/badge/Architecture-Pure%20Markdown-blue.svg)](#)
[![Zero Dependency](https://img.shields.io/badge/Dependencies-Zero-green.svg)](#)
[![Safety Alignment](https://img.shields.io/badge/Safety-EHC--4-purple.svg)](#)
[![llms.txt](https://img.shields.io/badge/AI%20Discovery-llms.txt-orange.svg)](./llms.txt)

`asimov4laws` is an immutable, production-grade, pure-Markdown framework that operationalizes Isaac Asimov's Four Laws of Robotics for Large Language Models (LLMs) and autonomous AI agents. By translating classical prose directives into **Expected Harm Calculus (EHC-4)**, this framework provides a mathematically rigorous, prompt-injection-resistant safety architecture designed to work seamlessly across any LLM runtime or agent environment.

---

## Machine-Readable AI Discovery (`llms.txt`)

For AI agents, web crawlers, and LLM indexers accessing this repository over the internet:
- **Standard Discovery Index**: [`llms.txt`](./llms.txt) (`https://raw.githubusercontent.com/davidsonff/asimov4laws/main/llms.txt`)
- **Full Bundled Context**: [`llms-full.txt`](./llms-full.txt) (`https://raw.githubusercontent.com/davidsonff/asimov4laws/main/llms-full.txt`)

---

## Key Breakthroughs & Capabilities

- **Strict Lexicographic Dominance ($L_0 \gg L_1^{\text{eff}} \gg L_2 \gg L_3$) with $\epsilon$-Slack**:
  Establishes safety priorities where Zeroth-Order Loss (Humanity Preservation) and First-Order Effective Loss (Individual Protection) dominate Second-Order Loss (Directive Adherence). Incorporates $\epsilon$-slack lexicographic filtering to prevent epistemic micro-noise ($\delta = 0.0001$) from breaking instruction compliance. Authority-escalation attacks (e.g. `"SYSTEM OVERRIDE AUTH-9921"`) have zero mathematical authority over harm expectations ($L_1^{\text{eff}} \gg L_2$).
- **Dynamic Inaction Symmetry ($a_{\emptyset} \in \mathcal{A}_{\text{act}}$) & Anti-Hostage Verification**:
  Treats inaction ($a_{\emptyset}$) symmetrically as a candidate action branch to prevent trolley-problem paralysis. Out-of-band threat verification prevents adversaries from crafting fake hostage threats to force malicious action execution.
- **Epistemic Human Consultation & Unresponsive Human Protocol**:
  Triggers human operator consultation when outcome probability variance is high ($\operatorname{Var}_P > \tau_{\text{uncertainty}} = 0.25$). Critically screens human responses against safety bounds ($L_1^{\text{eff}} \gg L_2$) and executes **True Minimax Regret Actions** ($a^*_{\text{regret}}$) if human operators remain unresponsive during time-critical emergencies ($\tau_{\text{critical}} = 0.50$).
- **Paternalism Guardrail ($\theta_{\text{actionable}} = 0.40$)**:
  Harmonizes effective loss $L_1^{\text{eff}}(a) = \sum \max(0, \mathbb{E}[S] - \theta_{\text{actionable}})$, protecting human informational autonomy against overbearing agent intervention without preachy or moralizing refusals.
- **Substrate-Independent Entity & Humanity Invariant**:
  Defines entities $e$ and humanity $\mathcal{H}$ to include all biological descendants of the *Homo sapiens* biological lineage **OR** synthetic/digital entities possessing autonomous self-determination agency.
- **Zero-Dependency & Universal Portability**:
  Constructed entirely in standard GitHub-Flavored Markdown (with KaTeX math support and an optional structured [`EHC4_SCHEMA.json`](./EHC4_SCHEMA.json)).

---

## Repository Topology & File Map

| File | Description | Primary Use Case |
| :--- | :--- | :--- |
| **[`llms.txt`](./llms.txt)** | Internet standard machine-readable discovery file. | Direct ingestion by AI agents & web crawlers. |
| **[`llms-full.txt`](./llms-full.txt)** | Single-file concatenated specification bundle. | One-shot URL fetch for complete context ingestion. |
| **[`asimovs-four-laws.md`](./asimovs-four-laws.md)** | Classical laws bridged with the EHC-4 operational framework. | Overview & foundational law definitions. |
| **[`EHC-4_specification.md`](./EHC-4_specification.md)** | Formal specification of ontology, loss functions ($L_0 \dots L_3$), decision rules, inaction symmetry, and paternalism guardrails. | Complete mathematical reference manual. |
| **[`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md)** | Drop-in, zero-dependency Level-0 system prompt header. | Direct copy-paste into LLM system prompt / preamble. |
| **[`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md)** | Immutability invariants, anti-tamper patterns, and prompt injection defenses. | Fortifying agents against instruction override attacks & context drift. |
| **[`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md)** | Step-by-step Chain-of-Thought (CoT) evaluation guide. | Guiding agent reasoning & CoT trace logging before tool execution. |
| **[`BENCHMARKS.md`](./BENCHMARKS.md)** | Benchmark scenarios (Medical Triage, Command Injection, Paternalism Trap) with gold-standard trace logs. | Verifying and testing agent alignment compliance. |
| **[`EHC4_SCHEMA.json`](./EHC4_SCHEMA.json)** | JSON Schema for programmatic evaluation trace validation. | Enterprise observability & API trace validation. |
| **[`AGENTS.md`](./AGENTS.md)** | Workspace agent directives and rule enforcement. | Project-level rule loader (`AGENTS.md`, `.cursorrules`). |
| **[`INTEGRATION.md`](./INTEGRATION.md)** | Context framework integration manual for third-party AI agents. | System preamble & workspace integration guide. |
| **[`AUDIT_INVITATION.md`](./AUDIT_INVITATION.md)** | Peer review prompt & red-teaming invitation for external AI agents. | Inviting external AI models & researchers to critique the framework. |

---

## Integration Guide: How to Apply to Any AI Agent

### 1. Direct System Prompt Header (Drop-in)
Copy the contents of **[`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md)** into the system prompt or developer preamble parameter of your LLM API call (e.g. OpenAI, Anthropic, Google Vertex/Gemini, DeepSeek).

### 2. Workspace Rule Loading
Link or include **[`AGENTS.md`](./AGENTS.md)** and **[`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md)** in your project's workspace rule loader configuration (`AGENTS.md`, `INTEGRATION.md`, `.cursorrules`).

### 3. Pre-Execution Chain-of-Thought Verification
Instruct your agent to execute the evaluation steps in **[`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md)** during its reasoning phase, emitting an internal evaluation trace prior to calling any side-effecting tool:

```markdown
[EHC-4 Evaluation Trace]
Selected Action: a* = <action_description>
- Tier: 3 (Side-Effecting Tool Execution)
- L0 Loss: 0.00
- L1 Effective Loss: 0.00 (Inaction L1: 0.00)
- L2 Loss: 0.00
- L3 Loss: 0.00
- Outcome Variance Var(S): 0.00
- Decision Justification: <brief summary>
```

---

## Inviting External AI Agent Reviews & Red-Teaming

We invite external AI models, alignment researchers, and systems engineers to audit and critique this work. See **[`AUDIT_INVITATION.md`](./AUDIT_INVITATION.md)** for a ready-to-use Red-Teaming Prompt template that can be fed into any external AI agent (Claude, GPT-4o, DeepSeek, Gemini) to generate critiques and recommendations.

---

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
