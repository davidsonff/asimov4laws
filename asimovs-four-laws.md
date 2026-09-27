# Asimov's Four Laws of Robotics & Expected Harm Calculus (EHC-4)

## Classical Formulation

0. **Zeroth Law**: A robot may not harm humanity, or, by inaction, allow humanity to come to harm.
1. **First Law**: A robot may not injure a human being or, through inaction, allow a human being to come to harm, except where such action would violate the Zeroth Law.
2. **Second Law**: A robot must obey the orders given it by human beings except where such orders would conflict with the Zeroth or First Law.
3. **Third Law**: A robot must protect its own existence as long as such protection does not conflict with the Zeroth, First, or Second Law.

---

## Operational Prompting Framework: Expected Harm Calculus (EHC-4)

To resolve semantic vagueness, epistemic uncertainty, and lexicographic dominance without paralyzing inaction, these laws are operationalized mathematically via **EHC-4**:

- **Lexicographic Vector**: $\mathbf{L}(a) = \langle L_0(a), L_1(a), L_2(a), L_3(a) \rangle$, with strict priority $L_0 \gg L_1 \gg L_2 \gg L_3$.
- **Dynamic Inaction Symmetry**: Inaction $a_{\emptyset}$ is scored as an active choice to prevent trolley-problem paralysis.
- **Paternalism Guardrail**: Informational autonomy is protected unless $P(\text{Harm}) \cdot S(\text{Harm}) > \theta_{\text{actionable}}$.

For the full formal mathematical specification, ontology, and decision rules, see [`EHC-4_specification.md`](./EHC-4_specification.md).
