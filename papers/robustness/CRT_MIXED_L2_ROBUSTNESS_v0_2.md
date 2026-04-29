> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: CLOSED. See [STATUS_GLOSSARY.md](../../STATUS_GLOSSARY.md).

# CRT Mixed Layer-2 Robustness Theorem — v0.2

**Date**: 2026-04-28 | **Status**: CLOSED

**Key change from v0.1**: Replaced source-count proxy with sealed Break/min-HS machinery throughout.

---

## $C_{\min}$ in the mixed setting

$$\mathcal{B}(a) = \{\mathrm{Break}(J) : J \in \mathcal{J}_{\mathrm{valid}}(P,a,\Pi)\}, \quad
C_{\min}(a) = \min\text{-HS-cost}(\mathcal{B}(a))$$

**Boundary cases**:
- Source-free $J$: $\mathrm{Break}(J) = \emptyset$ → min-HS cost $= +\infty$
- $\mathcal{J}_{\mathrm{valid}} = \emptyset$: $C_{\min}(a) = 0$

**Tier-2 atoms** (rule-derived, source-free $J^{int}$): $C_{\min}(a) = +\infty$.

**Tier-3 atoms** ($B_T$-sourced): $C_{\min}(a) < +\infty$.

**Mixed restricted cost**:
$$C_{\min}^{\mathrm{mix}}(P,\Pi) := \min_{a \in P^{\mathrm{Tier3}}} C_{\min}(a, P, \Pi)$$

---

## Theorems

**ML-R1 (Tier-2 isolation)**: Under C1+C2+C3 + standard declared-basis:
$$P \in \mathrm{SCSet} \Rightarrow \forall a \in P^{\mathrm{Tier2}}: C_{\min}(a) = +\infty$$
*Proof*: $\mathrm{Break}(J^{int}) = \emptyset$; empty break set has min-HS cost $+\infty$. □

**ML-R2 (Mixed threshold)**: $C_{\min}^{\mathrm{mix}}(P,\Pi) \geq \theta \iff \forall a \in P^{\mathrm{Tier3}}: C_{\min}(a) \geq \theta$.

**ML-R3 (Defense raises $C_{\min}$)**: Defense $\delta$ restricts $\mathcal{J}_{\mathrm{ext}}$.
Smaller break family → $C_{\min}^\delta(a) \geq C_{\min}(a)$. □

**ML-R4 (Institution floor)**: Institution $\iota$ enforcing min-cost $k$:
$C_{\min}^{\mathrm{mix},\iota}(P,\Pi) \geq k$. □

**ML-Main (Robustness decomposition)**:
Tier-2 contribution: $+\infty$ (structurally robust).
Tier-3 contribution: $C_{\min}^{\mathrm{mix},\delta}$ (defense-bounded).
Overall $C_{\min}(P,\Pi)$ determined by the least-robust Tier-3 atom.

---

## DeFi instance

| Audit claim | Break/min-HS formulation |
|---|---|
| Risk Steward 1-of-1 → $C_{\min}=1$ | Single-element break set: $\mathrm{Break}(J) = \{s\}$ |
| Multi-oracle raises $C_{\min}$ | Defense eliminates $J$ with $|\mathrm{break set}| < k$ |
| Tier-2 rule-derived robust | ML-R1: $\mathrm{Break}(J^{int}) = \emptyset$ |
| Institution gives floor | ML-R4: $\mathcal{J}^\iota_{\mathrm{ext}}$ forces min-HS cost $\geq k$ |

*End of CRT Mixed Layer-2 Robustness v0.2 — CLOSED.*
