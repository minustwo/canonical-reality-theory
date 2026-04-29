> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: CLOSED. See [STATUS_GLOSSARY.md](../../STATUS_GLOSSARY.md).

# CRT Execution Layer — Min-Cut Extension v0.2

**Date**: 2026-04-28 | **Status**: CLOSED

**Key change from v0.1**: Separated two cut semantics; corrected CAPO attribution.

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

**Refined Prop 2**:
$$C_{\min}^{\mathrm{ctrl},\mathrm{exec}} \leq C_{\min}^{\mathrm{ctrl},\mathrm{proto}} \leq C_{\min}^{\mathrm{ctrl},\mathrm{gov}}$$

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

## Layer-identification protocol

For any safety property $a$:
1. Enumerate $\mathcal{J}^{gov}$, $\mathcal{J}^{proto}$, $\mathcal{J}^{exec}$
2. Compute $C_{\min}^{\mathrm{break},\ell}$ and $C_{\min}^{\mathrm{ctrl},\ell}$ per layer
3. Identify dominant layer
4. Report $C_{\min}$ **with layer attribution**

Without step 3–4: correct number, wrong redesign target.

---

## Defense and institution

Defense $\delta$ restricts $\mathcal{J}^{exec}$: $C_{\min}^{\mathrm{ctrl},\mathrm{exec},\delta} \geq \theta$.
Institution $\iota$ (unconditional floor): $C_{\min}^{\mathrm{ctrl},\mathrm{exec},\iota} \geq k$.

Fork B/Class III: target $C_{\min}^{\mathrm{ctrl}} \geq \theta$ via defense/institution, not $+\infty$.

*End of CRT Execution Layer Min-Cut Extension v0.2 — CLOSED.*
*EL-1B: exec ≤ proto ≤ gov (control-plane cost). CAPO: execution-layer one-component control cut.*
