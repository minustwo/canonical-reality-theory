# CRT Mixed Layer-2 Robustness Theorem — v0.2

**Date**: 2026-04-28
**Status**: **CLOSED**

**Changes from v0.1**:
1. Replaced source-count proxy with sealed Break/min-HS machinery
2. $C_{\min}^{\mathrm{mix}}$ defined as Tier-3-restricted escape cost via $C_{\min}(a)$
3. Tier-2 atoms: $\mathrm{Break}(J^{int}) = \emptyset \Rightarrow C_{\min} = +\infty$
4. Defense/Institution expressed as threshold over $C_{\min}^{\mathrm{mix}} \geq \theta$

---

## 1. $C_{\min}$ machinery

**Sealed definition** (Break/min-HS):
$$\mathcal{B}(a) = \{\mathrm{Break}(J) : J \in \mathcal{J}_{\mathrm{valid}}(P,a,\Pi)\}, \quad C_{\min}(a) = \min\text{-HS-cost}(\mathcal{B}(a))$$

**Tier-2 atoms**: source-free $J_a^{int}$ → $\mathrm{Break}(J^{int}) = \emptyset$ → $C_{\min}(a) = +\infty$.

**Tier-3 atoms** ($B_T$-sourced): all valid $J$ have $\mathrm{Src}(J) \neq \emptyset$ → $C_{\min}(a) < +\infty$.

**Mixed restricted escape cost**:
$$\boxed{C_{\min}^{\mathrm{mix}}(P,\Pi) := \min_{a \in P^{\mathrm{Tier3}}} C_{\min}(a, P, \Pi)}$$

---

## 2. Main theorems

**ML-R1** (Tier-2 isolation): Under C1+C2+C3 + standard declared-basis:
$$P \in \mathrm{SCSet}_T(\Pi) \Rightarrow \forall a \in P^{\mathrm{Tier2}},\quad C_{\min}(a) = +\infty$$

**ML-R2** (Mixed robustness lower bound):
$$C_{\min}^{\mathrm{mix}}(P,\Pi) \geq \theta \iff \forall a \in P^{\mathrm{Tier3}},\quad C_{\min}(a,P,\Pi) \geq \theta$$

**ML-R3** (Defense raises $C_{\min}^{\mathrm{mix}}$): Defense $\delta$ restricts $\mathcal{J}_{\mathrm{ext}}$, reducing break family → $C_{\min}^\delta(a) \geq C_{\min}(a)$.

**ML-R4** (Institution provides floor): Institution $\iota$ enforcing min-HS cost $\geq k$ gives $C_{\min}^{\mathrm{mix},\iota}(P,\Pi) \geq k$.

**ML-Main** (Decomposition): For Class III theories under defense $\delta$, robustness is determined entirely by the least-robust Tier-3 atom.

---

## 3. RT-OQ-2 answered

> Does mixed Layer-2 representation extend to finite-$C_{\min}$ robustness?

**Yes**. Three parts:
1. Tier-2 atoms: structurally robust for free ($\mathrm{Break}(J^{int}) = \emptyset$)
2. Tier-3 atoms: $C_{\min}^{\mathrm{mix}} \geq \theta$ via defense $\delta$ or institution $\iota$
3. Bound is tight: adversary can simultaneously corrupt exactly $\theta$ break-set elements

---

## 4. DeFi connection (Break/min-HS language)

| Audit claim | Formal backing |
|---|---|
| Multi-oracle raises $C_{\min}$ | Defense $\delta$ eliminates $J$ with break sets $< k$; min-HS cost $\geq k$ |
| Tier-2 rule conclusions robust | ML-R1: $\mathrm{Break}(J^{int}) = \emptyset \Rightarrow C_{\min} = +\infty$ |
| Institution provides floor | ML-R4: institutional $\mathcal{J}^\iota$ forces min-HS cost $\geq k$ |

---

*End of CRT Mixed Layer-2 Robustness v0.2 — CLOSED.*
*$C_{\min}$ uses sealed Break/min-HS machinery throughout.*
