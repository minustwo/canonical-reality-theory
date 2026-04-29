> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: CLOSED. See [STATUS_GLOSSARY.md](../../STATUS_GLOSSARY.md).
>
> **Scope note**: This theorem addresses bounded extractor-certifiable
> negation-as-absence (R0c). It does not address CJC (Circular Justification
> Consistency), which is an independent obstruction. See STATUS_GLOSSARY.md for CJC definition.

# CRT Negation-as-Absence Reformulation — General Theorem v0.2

**Date**: 2026-04-28 | **Status**: CLOSED

**Scope**: Bounded extractor-certifiable NAA (R0c). Not arbitrary default negation.

---

## The problem

Operator $F_i$ with negation-as-absence firing condition:
$$F_i(P) \ni a \quad\text{if}\quad \varphi^+(P) \wedge \neg\phi(P)$$

**R0c violation**: $\neg\phi(P)$ depends on atom absence, not membership.

---

## Reformulation schema

**Step 1**: Name the absence (outcome-named, not raw negation):
$$\mathrm{AbsenceAtom}_i(c, t_0, t_1) \in \Sigma_T$$

**Step 2**: Extractor semantics (typing contract, positive right-hand side):
$$\mathrm{AbsenceAtom}_i(c,t_0,t_1) \Rightarrow \mathrm{trigger}(c,t_0) \wedge t_1 = t_0 + \tau_i$$

**Step 3**: Reformulated operator:
$$F_i^+(P) \ni a \quad\text{if}\quad \Gamma_{\varphi^+} \subseteq P \wedge \mathrm{AbsenceAtom}_i(c,t_0,t_1) \in P$$

---

## Theorem (NAA-to-Positive Extractor Reformulation)

Assume:
- **(A1)** Bounded extractor-certifiability: $\neg\phi_i$ decidable by finite extractor over $(c, t_0, t_1)$
- **(A2)** Positive absence atom: $\mathrm{AbsenceAtom}_i \in \mathrm{At}_T$, typing contract positive
- **(A3)** $B_T$-source support (not `int_base`)
- **(A4)** Extractor consistency: absence atom declared only when absence confirmed
- **(A5)** Equivariant syntactic naming
- **(A6)** Declared certificate basis

**Then $F_i^+$ satisfies R0a–R0e** (LocalExplain holds). □

**Corollary**: If every NAA operator in $\mathcal{F}$ satisfying A1–A6 is reformulated,
the resulting $\mathcal{F}^+$ satisfies LocalExplain($\mathcal{F}^+$).

---

## Key properties

**Fixed-horizon positivity**: $F_i^+$ is $\preceq$-monotone in $P$ at fixed $\Pi$.
Under evidence refinement $\Pi' \supseteq \Pi$: extractor may retract absence atom.
$\mathcal{J}_{\mathrm{valid}}$ must be recomputed at each horizon (consistent with CRT Stack Interface v0.2).

**Bridge corollary**: LocalExplain($\mathcal{F}^+$) is one condition for ULift$^{sat}$.
DeclCompat is additionally required for Bridge A (not automatic from A1–A6).

---

## Scope boundary

Schema applies when: bounded window (A1), extractor decidability (A1),
meaningful absence event (A2), $B_T$-source available (A3), consistency guaranteed (A4),
equivariant naming (A5).

Schema does NOT apply: unbounded window; absence requires `int_base`; no Layer-2 source
can certify absence; consistency (A4) cannot be guaranteed.

**CJC note**: If the resulting justification system still has globally circular
justification consistency (CJC), NAA reformulation does not remove that obstruction.
CJC is an independent boundary condition.

---

## ICT v2.1 instance

| Original rule | Absence atom | Reformulated |
|---|---|---|
| $\mathrm{Liq\_sweep} \wedge \neg\exists\mathrm{BOS}[t_0,t_1]$ | $\mathrm{ICT\_confirmation\_failed}(l,t_0,t_1)$ | R-Exh⁺ |

---

## What this theorem does NOT resolve

- `int_base` certification of absence atoms (Tier-3, $B_T$-sourced)
- CertReach / TracedSCSet issues (Fork B persists)
- DeclCompat (separate Layer-2 condition)
- CJC (independent obstruction)

*End of CRT NAA Reformulation General Theorem v0.2 — CLOSED.*
*Scope: bounded extractor-certifiable NAA (R0c). Not CJC.*
