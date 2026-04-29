# CRT Robustness and Execution

This directory contains technical reports on mixed Layer-2 robustness,
negation-as-absence reformulation, and execution-layer min-cut analysis.

**Publication status**: Technical-report / research-archive material.
These files are not peer-reviewed publications.

> "Sealed" and "Closed" are internal archive-status labels.
> They do not indicate external peer review.
> See [`STATUS_GLOSSARY.md`](../../STATUS_GLOSSARY.md) for definitions.

---

## Key distinction

$$C_{\min}^{\mathrm{break}} \neq C_{\min}^{\mathrm{ctrl}}$$

- **$C_{\min}^{\mathrm{break}}$**: source-disable / invalidation cost (defender-side, ∀-hitting).
  Defined as minimum hitting-set cost over the break family.
  **Monotone direction**: break chain goes exec ≤ proto ≤ gov.

- **$C_{\min}^{\mathrm{ctrl}}$**: control / capture / misconfiguration path cut cost (attacker-side, ∃-path).
  **Single-layer chain is false in general** (counterexample X1).
  **Cumulative chain reverses**: $C_{\min}^{\mathrm{ctrl},\leq\mathrm{gov}} \leq C_{\min}^{\mathrm{ctrl},\leq\mathrm{proto}} \leq C_{\min}^{\mathrm{ctrl},\leq\mathrm{exec}}$.

The two semantics point in **opposite directions** under layer ordering because
break uses $\forall$+min-HS (anti-monotone) while ctrl uses $\exists$+min-covering (co-monotone).

---

## Files

- **[`CRT_EXECUTION_LAYER_MINCUT_v0_3.md`](CRT_EXECUTION_LAYER_MINCUT_v0_3.md)** (CLOSED) — **Canonical version.**
  Corrects v0.2. EL-1B-break holds; single-layer ctrl chain falsified by X1;
  cumulative ctrl reverse chain proved. DeFi CAPO/AgentHub attribution correct.

- **[`CRT_EXECUTION_LAYER_MINCUT_v0_2.md`](CRT_EXECUTION_LAYER_MINCUT_v0_2.md)** (SUPERSEDED) — Do not cite.
  Retained for audit trail only.

- **[`CRT_MIXED_L2_ROBUSTNESS_v0_2.md`](CRT_MIXED_L2_ROBUSTNESS_v0_2.md)** (CLOSED) — Mixed Layer-2 robustness theorems.
  Tier-2 atoms structurally robust. Tier-3 requires defense or institution.

- **[`CRT_NAA_REFORMULATION_THEOREM_v0_2.md`](CRT_NAA_REFORMULATION_THEOREM_v0_2.md)** (CLOSED) — NAA reformulation.
  Scope: bounded extractor-certifiable negation-as-absence (R0c).

---

*See [`papers/bridge/`](../bridge/) for bridge theorem files.*
