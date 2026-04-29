> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: SEALED (version-locked). See [STATUS_GLOSSARY.md](../../STATUS_GLOSSARY.md).

# CRT Bridge Theorem — Final Form v1.0.1

**Date**: 2026-04-28
**Status**: **SEALED**
**Purpose**: Consolidated statement of the CRT Bridge Theorem.

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

**C1 — LocalExplain**: Each $F_i$ has a certificate relation $\mathrm{Cert}_i$ satisfying R0a–R0e
(soundness, addition completeness, positivity, equivariance, syntactic declared basis).

**C2 — DeclCompat**: $J_{\Gamma \to a}^{int} \in \mathcal{J}_{\mathrm{declared}}(P^*, a, \Pi)$.

**C3 — NDLift**: Source-free valid $J_a$ is $\mathcal{D}_T^{int}$-certified.

**C4 — DeclComplete**: $P \in \mathcal{P}_T(\Pi) \Rightarrow \mathrm{CertClosed}_{\mathcal{F}}(P)$.

**C5 — ULift$^{sat}_T$**: $\forall P \in \mathrm{UnbreakSet}_T(\Pi): F(P) \subseteq P$.
Sufficient: $\mathrm{C1} \wedge \mathrm{C3} \wedge \mathrm{C4} \Rightarrow \mathrm{C5}$.

**Terminology note (Bridge Hierarchy v0.3)**: C5 here = ULift-sat (sufficient route).
The primitive right-bridge condition is **C5_R**: UnbreakSet ⊆ SCSet.

---

## 3. Main theorem: Bridge Sandwich

**Theorem** (CRT Bridge Sandwich). Under C1–C5:

$$\boxed{\mathrm{TracedSCSet}_T(\Pi)
\;\subseteq_{\mathrm{C1} \wedge \mathrm{C2}}\;
\mathrm{UnbreakSet}_T(\Pi)
\;\subseteq_{\mathrm{C5}}\;
\mathrm{SCSet}_T(\Pi)}$$

*Left inclusion (Bridge A, C1+C2)*: Traced atoms compile to source-free valid justifications →
$C_{\min}^{\mathrm{weak}}(P,\Pi) = +\infty$ → $P \in \mathrm{UnbreakSet}$. □

*Right inclusion (C5 + Bridge B)*: UnbreakSet + C5 → $F(P) \subseteq P$ →
$\mathrm{SC}_T(P) = 1$ → $P \in \mathrm{SCSet}$. □

---

## 4. Conditional equalities

**Trace-completeness** (C6, general form):
$$\mathrm{SCSet} \subseteq \mathrm{CertReach} \iff \mathrm{SCSet} = \mathrm{TracedSCSet}$$

**Full Bridge** (C1+C2+C5_R+C6): $\mathrm{TracedSCSet} = \mathrm{UnbreakSet} = \mathrm{SCSet}$.

**Canonical uniqueness** (property $(4)$): $|\mathrm{SCSet}_T(\Pi)| = 1$.
Under CWA: singleton at any non-empty $\Pi$.

---

## 5. Rule-closed structure theorem

If $\mathcal{F}_{\mathrm{rule}}$ mirrors $I_T^{core}$:
$\mathrm{SCSet}_{T,\mathcal{F}_{\mathrm{rule}}}^+(\Pi) = \mathcal{P}_T^+(\Pi)$.

Bridge sandwich: $\mathrm{TracedSCSet} \subseteq \mathrm{UnbreakSet} \subseteq \mathcal{P}_T^+(\Pi)$.

---

## 6. NAA Reformulation integration

If $F_i$ has bounded extractor-certifiable NAA premise (A1–A6), the reformulated
$F_i^+$ satisfies R0a–R0e. C1 can be established via this schema.

---

## 7. ICT instance

| Condition | Status |
|---|---|
| C1 LocalExplain | ✓ |
| C2 DeclCompat | ✓ |
| C3 NDLift | ✓ |
| C4 DeclComplete | ✓ |
| C5 ULift^sat | ✓ (automatic: rule-generated $\mathcal{F}$) |
| Property $(4)$ | ✓ (CWA_ICT) |

Bridge sandwich (Fork B + CWA_ICT):
$$\mathrm{TracedSCSet} \subseteq \mathrm{UnbreakSet} \subseteq \{P_{\min}(\Pi)\}$$

Under Fork B, non-trivial $\Pi$: Tier-3 atoms block TracedSCSet and UnbreakSet.
ICT robustness: finite $C_{\min}$, defense (Layer 5), institution (Layer 6).

---

*End of CRT Bridge Theorem — Final Form v1.0.1. SEALED.*
