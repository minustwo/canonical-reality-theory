# CRT Condition Independence — v0.2

**Date**: 2026-04-28
**Status**: **CLOSED**

**Changes from v0.1**:
1. C1 witness: $T_{\mathrm{bb}}$ (black-box monotone operator, no declared Cert scheme, invokes R0e)
2. C2 witness: $T_{\mathrm{mismatch}}$ — explicit $J^{int} \notin \mathcal{J}_{\mathrm{declared}}$ witness (closes B-OQ-1)
3. C5_R witness: R6-lift failure ($\{a\} \in \mathrm{UnbreakSet} \setminus \mathrm{SCSet}$)
4. C3/C4 section: sufficient-route minimality only, not primitive bridge
5. CI-OQ-2 resolved: $T_{\mathrm{bb}}$ has non-empty SCSet

---

## 1. Theorem CI (Condition Independence)

$$\boxed{\forall i \in \{\mathrm{C1, C2, C5\_R, C6}\},\quad
\{\mathrm{C1,C2,C5\_R,C6}\} \setminus \{C_i\} \not\Rightarrow
\text{the conclusion that } C_i \text{ supports}}$$

---

## 2. Witnesses for primitive bridge conditions

### C1 — $T_{\mathrm{bb}}$ (black-box operator)

Monotone set map supplied extensionally only; no declared certificate relation $\mathrm{Cert}_{F_{\mathrm{bb}}}$. R0e requires a syntactic/declared scheme — a black-box function has none. Without C1, trace compilation has no $\Gamma$ to record; all outputs tagged `uncertified_seed`.

**Non-vacuity**: $T_{\mathrm{bb}}$ has non-empty SCSet; TracedSCSet is empty. C1 is necessary for the proof mechanism, even if inclusion holds vacuously.

### C2 — $T_{\mathrm{mismatch}}$

Rule $F_1: \{b\} \Rightarrow a$. Declared family: $\mathcal{J}_{\mathrm{declared}}(P, a, \Pi) = \{J_{c \to a}\}$ only ($J_{b \to a}$ not declared). Traced saturation gives $\tau(a) = (F_1, \{b\})$; compiled $J^{int} = J_{b \to a} \notin \mathcal{J}_{\mathrm{declared}}$; hence $J^{int} \notin \mathcal{J}_{\mathrm{valid}}$; no source-free valid $J$ for $a$.
$$P^* \in \mathrm{TracedSCSet} \setminus \mathrm{UnbreakSet}$$
**B-OQ-1 CLOSED**.

### C5_R — R6-lift failure

Atoms $\{a\}$; rule $F_1: \{a\} \Rightarrow b$. Source-free $J_a$ for $a$: $C_{\min}^{\mathrm{weak}}(\{a\}) = +\infty \Rightarrow \{a\} \in \mathrm{UnbreakSet}$. But $F_1(\{a\}) = \{a, b\} \not\subseteq \{a\} \Rightarrow \{a\} \notin \mathrm{SCSet}$.

### C6 — $T_{\mathrm{ICT}}^{v2.1}$ Fork B

$P_{\mathrm{wit}} \in \mathrm{SCSet}$; Tier-3 atom → `uncertified_seed` → $P_{\mathrm{wit}} \notin \mathrm{TracedSCSet}$.

---

## 3. Pairwise independence

| Condition | Fails | Others hold | Witness |
|---|---|---|---|
| C1 | ✗ | C2,C5_R,C6 ✓ | $T_{\mathrm{bb}}$ |
| C2 | ✗ | C1,C5_R,C6 ✓ | $T_{\mathrm{mismatch}}$ |
| C5_R | ✗ | C1,C2,C6 ✓ | R6-lift |
| C6 | ✗ | C1,C2,C5_R ✓ | $T_{\mathrm{ICT}}^{v2.1}$ Fork B |

**All four primitive conditions are independently necessary.**

---

## 4. Sufficient-route minimality (C3, C4)

C3 (NDLift) and C4 (DeclComplete) are necessary for the ULift route to C5_R — not for C5_R as a primitive.

- Without C3: phantom $J^{ph}$ makes ULift fail ($T_{\mathrm{ph}}$)
- Without C4: $\mathcal{J}_{\mathrm{declared}}$ gap makes ULift fail ($T_{\mathrm{incomplete}}$)

---

*End of CRT Condition Independence v0.2 — CLOSED.*
*All four primitive bridge conditions formally proved necessary.*
*B-OQ-1 CLOSED via $T_{\mathrm{mismatch}}$ witness.*
