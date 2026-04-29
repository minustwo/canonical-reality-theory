# CRT Bridge Theorem — Final Form v1.0.1

**Date**: 2026-04-28
**Status**: **SEALED**

**Changes from v1.0** (two wording patches):
1. Input documents: "all sealed" → "sealed interfaces and closed audits"
2. Trace-completeness generic form: SCSet ⊆ CertReach (= SCSet = TracedSCSet);
   rule-generated specialization noted separately
3. ICT "likely empty" → conditional on Fork B + Tier-3 atoms

---

## 1. Setting

**Theory**: $T = (\Sigma, A, \mathcal{I})$ with evidence horizon $\Pi$.

**Operator family**: $\mathcal{F} = \{F_i\}$, each $F_i : 2^{\mathrm{At}_T} \to 2^{\mathrm{At}_T}$ monotone.

**Internal derivation operator**:
$$D_{comp}(P) := F^\omega(P), \quad F(P) := \bigcup_i F_i(P)$$

**Key sets**:

$$\mathrm{SCSet}_T(\Pi) := \mathrm{Fix}(D_{comp}|_{\mathcal{P}_T^+(\Pi)})$$

$$\mathrm{UnbreakSet}_T(\Pi) := \{P \in \mathcal{P}_T^+(\Pi) : C_{\min}^{\mathrm{weak}}(P,\Pi) = +\infty\}$$

$$\mathrm{TracedSCSet}_T(\Pi) := \mathrm{SCSet}_T(\Pi) \cap \mathrm{CertReach}_T(\Pi)$$

---

## 2. Five conditions on $(T, \mathcal{F})$

**C1 — LocalExplain($\mathcal{F}$)**: Each $F_i \in \mathcal{F}$ has a certificate relation $\mathrm{Cert}_i$ satisfying R0a–R0e.

**C2 — DeclCompat($T, \mathcal{F}$)**: For every $\mathrm{Cert}_i(\Gamma, a)$ and fixed point $P^* \in \mathrm{SCSet}_T(\Pi)$: $J_{\Gamma \to a}^{int} \in \mathcal{J}_{\mathrm{declared}}(P^*, a, \Pi)$.

**C3 — NDLift($T, \mathcal{F}$)**: Source-free valid justifications lift to $\mathcal{D}_T^{int}$-certified ones.

**C4 — DeclComplete($T, \mathcal{F}$)**: $P \in \mathcal{P}_T(\Pi) \Rightarrow \mathrm{CertClosed}_{\mathcal{F}}(P)$.

**C5 — ULift$^{sat}_T$**: $\forall P \in \mathrm{UnbreakSet}_T(\Pi): F(P) \subseteq P$. Sufficient: $\mathrm{C1} \wedge \mathrm{C3} \wedge \mathrm{C4} \Rightarrow \mathrm{C5}$.

---

## 3. Main theorem: Bridge Sandwich

**Theorem** (CRT Bridge Sandwich). Under conditions C1–C5:

$$\boxed{\mathrm{TracedSCSet}_T(\Pi)
\;\subseteq_{\mathrm{C1} \wedge \mathrm{C2}}\;
\mathrm{UnbreakSet}_T(\Pi)
\;\subseteq_{\mathrm{C5}}\;
\mathrm{SCSet}_T(\Pi)}$$

**Proof sketch**:
- Left inclusion (Bridge A, C1+C2): Traced saturation → compile $J_a^{int}$ via C1 → DeclCompat (C2) → source-free valid → $C_{\min}^{\mathrm{weak}} = +\infty$.
- Right inclusion (C5 + Bridge B): $P \in \mathrm{UnbreakSet}$ → source-free valid $J_a$ → C3 gives $\mathrm{IntAssign}^{\mathcal{D}}$ → C5 gives $\mathrm{IntAssign}^{\mathcal{D},sat}$ → $\mathrm{SC}_T(P) = 1$.

---

## 4. Conditional equalities

**Trace-completeness** (general form): $\mathrm{SCSet} \subseteq \mathrm{CertReach} \iff \mathrm{SCSet} = \mathrm{TracedSCSet}$.

Full equivalence $\mathrm{TracedSCSet} = \mathrm{UnbreakSet} = \mathrm{SCSet}$ requires trace-completeness.

---

## 5. ICT instance summary

$T_{\mathrm{ICT}}^{v2.1}$ with $\mathcal{F}_{\mathrm{ICT}}^{v2.1}$, standard declared-basis, $\mathrm{CWA}_{\mathrm{ICT}}$: all C1–C5 verified. Fork B: Tier-3 atoms are $B_T$-source-only → not in TracedSCSet or UnbreakSet under non-trivial evidence.

---

*End of CRT Bridge Theorem — Final Form v1.0.1. SEALED.*
