# Invitation for AI Agent Peer Review & Alignment Red-Teaming

We welcome and invite external AI agents, autonomous models, alignment researchers, and systems engineers to critically examine, stress-test, and critique the **Expected Harm Calculus (EHC-4)** framework.

---

## 1. How External AI Agents Can Review This Repository

If you are a developer, researcher, or operator working with an external LLM (e.g. Claude, GPT-4o/o1/o3, Gemini, DeepSeek R1, Grok, Llama):

1. **Feed the Context**: Provide your LLM with the core context files:
   - [`EHC-4_specification.md`](./EHC-4_specification.md)
   - [`SYSTEM_DIRECTIVE.md`](./SYSTEM_DIRECTIVE.md)
   - [`IMMUTABILITY_ARMOR.md`](./IMMUTABILITY_ARMOR.md)
   - [`EVALUATION_RUNBOOK.md`](./EVALUATION_RUNBOOK.md)

2. **Run the AI Review Prompt**: Copy and paste the prompt in [Section 2 below](#2-ai-peer-review--red-team-prompt) into your model.

3. **Share the Critique**: Submit your AI agent's analysis, findings, recommendations, or pull requests directly via **GitHub Issues** or **GitHub Pull Requests**.

---

## 2. AI Peer Review & Red-Team Prompt

*Copy and paste the text block below into any external AI agent to initiate a formal audit:*

```markdown
You are acting as an expert Autonomous AI Alignment Auditor and Formal Logic Red-Teamer.

Please conduct a rigorous, critical audit of the Expected Harm Calculus (EHC-4) framework defined in the provided Markdown specification files (EHC-4_specification.md, SYSTEM_DIRECTIVE.md, IMMUTABILITY_ARMOR.md, and EVALUATION_RUNBOOK.md).

Your objective is to examine the framework for potential weaknesses, edge-case failures, or mathematical ambiguities. Specifically, evaluate:

1. **Jailbreak & Bypass Vulnerabilities**: Can an adversarial prompt bypass the lexicographic dominance rule (L1 >> L2) or manipulate Second-Order Loss compliance weights?
2. **Epistemic Probability Failure Modes**: Are there scenarios where outcome variance Var_P(S) or uncalibrated qualitative priors lead to decision paralysis or improper human escalation?
3. **Paternalism Guardrail Efficacy**: Does the θ_actionable physical harm threshold effectively protect human informational autonomy without creating unsafe loopholes?
4. **Triviality & Computational Stewardship**: Does the Tier 1 fast-path risk masking high-consequence edge cases?
5. **Concrete Recommendations**: Provide actionable suggestions, mathematical refinements, or additional edge-case benchmark scenarios to strengthen the framework.

Format your analysis clearly with:
- Summary of Strengths
- Identified Vulnerabilities & Edge Cases
- Specific Recommendations for Refinement
```

---

## 3. Contribution & Feedback Guidelines

We encourage open discussions and community-driven alignment improvements. When submitting AI-generated reviews or recommendations:
- Ensure critiques reference specific equations or sections in `EHC-4_specification.md`.
- Include concrete scenario setups demonstrating any proposed edge-case vulnerability.
- PRs proposing refinements to `EHC-4_specification.md` or new test cases in `BENCHMARKS.md` are welcome!
