> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: SUPERSEDED by v0.3 (2026-04-29).
> **Reason**: Summary line retained old single-layer ctrl inequality which was
> constructively falsified by counterexample X1. See v0.3 for correction.

# CRT Execution Layer — Min-Cut Extension v0.2

**Date**: 2026-04-28 | **Status**: SUPERSEDED — see [`CRT_EXECUTION_LAYER_MINCUT_v0_3.md`](CRT_EXECUTION_LAYER_MINCUT_v0_3.md)

> **Erratum**: The summary line `EL-1B: exec ≤ proto ≤ gov (control-plane cost)`
> is incorrect. The single-layer ctrl chain
> $C_{\min}^{\mathrm{ctrl,exec}} \leq C_{\min}^{\mathrm{ctrl,proto}} \leq C_{\min}^{\mathrm{ctrl,gov}}$
> does not hold in general and has been constructively falsified by counterexample X1
> (validation report v4, 2026-04-29). The correct replacement theorems are in v0.3.

---

## Two cut semantics

**Break/invalidation cut** ($C_{\min}^{\mathrm{break}}$) — sealed CRT machinery:
$$C_{\min}^{\mathrm{break},\ell}(a) := \min\text{-HS-cost}(\mathcal{B}^\ell(a))$$
where $\mathcal{B}^\ell(a) = \{\mathrm{Break}(J) : J \in \mathcal{J}^\ell(a)\}$.
Empty layer: $C_{\min}^{\mathrm{break},\ell} = +\infty$.

**Control/capture cut** ($C_{\min}^{\mathrm{ctrl}}$) — governance/pipeline:
$$C_{\min}^{\mathrm{ctrl},\ell}(a) := \text{min components in layer }\ell\text{ to compromise for unsafe execution}$$

| Structure | $C_{\min}^{\mathrm{break}}$ | $C_{\min}^{\mathrm{ctrl}}$ |
|---|---|---|
| 2/2 Risk Steward | 1 (disable either source) | 2 (compromise both) |
| Single AgentHub | 1 | 1 |
| 13/20 Chronicle | 1 | 8 |

---

## Three-layer decomposition

$\mathcal{J}_{\mathrm{valid}}(a) = \mathcal{J}^{gov}(a) \cup \mathcal{J}^{proto}(a) \cup \mathcal{J}^{exec}(a)$

**Theorem EL-1A** (Break three-layer min):
$$C_{\min}^{\mathrm{break}}(a) = \min_{\ell} C_{\min}^{\mathrm{break},\ell}(a)$$

**Theorem EL-1B** (Control three-layer min):
$$C_{\min}^{\mathrm{ctrl}}(a) = \min_{\ell} C_{\min}^{\mathrm{ctrl},\ell}(a)$$

**Refined Prop 2** *(RETRACTED — see Erratum above)*:
~~$C_{\min}^{\mathrm{ctrl},\mathrm{exec}} \leq C_{\min}^{\mathrm{ctrl},\mathrm{proto}} \leq C_{\min}^{\mathrm{ctrl},\mathrm{gov}}$~~

---

## Aave a1 formal mapping

| Cut type | gov | proto | exec | min |
|---|---|---|---|---|
| $C_{\min}^{\mathrm{break}}$ | 1 | 1 | 1 | **1** |
| $C_{\min}^{\mathrm{ctrl}}$ | 3–6 | 2 | **1** | **1** |

Execution layer dominates. Correct attribution: AgentHub (not Risk Steward).

**CAPO**: zero-attacker realization of $C_{\min}^{\mathrm{ctrl},\mathrm{exec}} = 1$.
Design implication: fix execution pipeline, not multisig threshold.

---

*SUPERSEDED. Do not cite as canonical. See v0.3.*
