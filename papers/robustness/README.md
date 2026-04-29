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

- **$C_{\min}^{\mathrm{break}}$**: source-disable / invalidation cost.
  Defined as minimum hitting-set cost over the break family
  $\mathcal{B}(a) = \{\mathrm{Break}(J) : J \in \mathcal{J}_{\mathrm{valid}}\}$.

- **$C_{\min}^{\mathrm{ctrl}}$**: control / capture / misconfiguration path cut cost.
  Execution Layer v0.2 defines EL-1B:
  $C_{\min}^{\mathrm{ctrl,exec}} \leq C_{\min}^{\mathrm{ctrl,proto}} \leq C_{\min}^{\mathrm{ctrl,gov}}$.

These are genuinely independent: a system can satisfy $C_{\min}^{\mathrm{break}} \geq \theta$
while $C_{\min}^{\mathrm{ctrl}} < \theta$ (DeFi CAPO/AgentHub is the canonical instance).

---

## Files

- **`CRT_MIXED_L2_ROBUSTNESS_v0_2.md`** (CLOSED) — Mixed Layer-2 robustness theorems.
  Tier-2 atoms structurally robust ($\mathrm{Break}(J^{int}) = \emptyset \Rightarrow C_{\min} = +\infty$).
  Tier-3 robustness requires defense or institution.
  $C_{\min}$ uses sealed Break/min-HS machinery, not source-count proxy.

- **`CRT_EXECUTION_LAYER_MINCUT_v0_2.md`** (CLOSED) — Execution Layer min-cut.
  Separates $C_{\min}^{\mathrm{break}}$ (invalidation) from $C_{\min}^{\mathrm{ctrl}}$
  (control/capture). EL-1B: execution layer dominates in composed systems.
  DeFi CAPO/AgentHub attribution corrected to execution-layer one-component control cut.

- **`CRT_NAA_REFORMULATION_THEOREM_v0_2.md`** (CLOSED) — NAA reformulation.
  Scope: bounded extractor-certifiable negation-as-absence (R0c).
  Does not address CJC (Circular Justification Consistency), which is an
  independent obstruction.

---

*See [`papers/bridge/`](../bridge/) for bridge theorem files.*
