> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: CLOSED — supersedes v0.2.
> **Reason**: EL-1B ctrl-chain corrected after validation report v4 (2026-04-29).
> v0.2 separated break/control semantics correctly but retained the old single-layer
> ctrl inequality in summary wording. v0.3 replaces it with the v4-corrected theorem split.

# CRT Execution Layer — Min-Cut Extension v0.3

**Date**: 2026-04-29 | **Status**: CLOSED — supersedes v0.2

---

## 0. Correction summary

v0.2 (2026-04-28) correctly separated $C_{\min}^{\mathrm{break}}$ from $C_{\min}^{\mathrm{ctrl}}$
but its summary line retained the old single-layer ctrl chain:

$$C_{\min}^{\mathrm{ctrl,exec}} \leq C_{\min}^{\mathrm{ctrl,proto}} \leq C_{\min}^{\mathrm{ctrl,gov}} \quad \textbf{[INCORRECT — see §3]}$$

This chain has been **constructively falsified** by counterexample X1 (validation report v4,
§5). v0.3 replaces it with the three-theorem split below.

### Theorem status table

| Label | Statement | Status |
|---|---|---|
| **EL-1B-break** | $C_{\min}^{\mathrm{break,exec}} \leq C_{\min}^{\mathrm{break,proto}} \leq C_{\min}^{\mathrm{break,gov}}$ | **Theorem** |
| **EL-1B-ctrl-single** | $C_{\min}^{\mathrm{ctrl,exec}} \leq C_{\min}^{\mathrm{ctrl,proto}} \leq C_{\min}^{\mathrm{ctrl,gov}}$ | **False in general — X1 counterexample** |
| **EL-1B-ctrl-cumulative** | $C_{\min}^{\mathrm{ctrl,\leq gov}} \leq C_{\min}^{\mathrm{ctrl,\leq proto}} \leq C_{\min}^{\mathrm{ctrl,\leq exec}}$ | **Theorem** |
| **Exec dominance** | $C_{\min}^{\mathrm{ctrl}} = C_{\min}^{\mathrm{ctrl,exec}}$ when exec path is lowest-cost | Conditional regime |

---

## 1. Three cut semantics

### 1.1 Break / invalidation cut (defender-side, ∀-hitting)

$$\mathcal{B}^\ell(a) := \{\mathrm{Break}(J) : J \in \mathcal{J}^\ell(a)\}$$
$$C_{\min}^{\mathrm{break},\ell}(a) := \min\text{-HS-cost}(\mathcal{B}^\ell(a))$$

Semantics: defender must hit **all** valid proofs simultaneously.
Empty layer: $\mathcal{J}^\ell = \emptyset \Rightarrow C_{\min}^{\mathrm{break},\ell} = +\infty$.

### 1.2 Single-layer ctrl cut (attacker-side, ∃-path, layer-restricted)

$$C_{\min}^{\mathrm{ctrl},\ell}(a) := \min\{|S| : S \subseteq \mathrm{Comp}(\ell),\; \exists J \in \mathcal{J}^\ell(a),\; J \subseteq S\}$$

Semantics: attacker compromises only layer-$\ell$ components to force an unsafe
execution path entirely within that layer.

### 1.3 Cumulative ctrl cut (attacker-side, ∃-path, cross-layer)

$$C_{\min}^{\mathrm{ctrl},\leq\ell}(a) := \min\{|S| : S \subseteq \mathrm{Comp}(\leq\ell),\; \exists J \in \mathcal{J}^{\leq\ell}(a),\; J \subseteq S\}$$

where $\mathrm{Comp}(\leq\ell) := \bigcup_{\ell' \leq \ell} \mathrm{Comp}(\ell')$.
Semantics: attacker may compromise components across all layers up to $\ell$.

**Key distinction**: Break uses $\forall$+min-HS (anti-monotone in $\mathcal{J}$);
ctrl uses $\exists$+min-covering (co-monotone in $\mathrm{Comp}$).
They point in **opposite directions** under layer ordering.

---

## 2. EL-1B-break theorem

**Theorem EL-1B-break**:

Under $\mathcal{J}^{\mathrm{exec}} \subseteq \mathcal{J}^{\mathrm{proto}} \subseteq \mathcal{J}^{\mathrm{gov}}$ (L0):

$$\boxed{C_{\min}^{\mathrm{break,exec}}(a) \leq C_{\min}^{\mathrm{break,proto}}(a) \leq C_{\min}^{\mathrm{break,gov}}(a)}$$

**Proof**: By min-HS anti-monotonicity (L1): $A \subseteq B \Rightarrow \min\text{-HS}(A) \leq \min\text{-HS}(B)$.
Apply twice to L0. $\square$

---

## 3. Single-layer ctrl chain is false — Counterexample X1

The chain $C_{\min}^{\mathrm{ctrl,exec}} \leq C_{\min}^{\mathrm{ctrl,proto}} \leq C_{\min}^{\mathrm{ctrl,gov}}$ **does not hold in general**.

**Counterexample X1** (minimum three-layer witness):

- $\mathrm{Comp}(\mathrm{exec}) = \{e_1, e_2, e_3\}$
- $\mathrm{Comp}(\mathrm{proto}) = \{p_1, p_2\}$
- $\mathrm{Comp}(\mathrm{gov}) = \{g_1\}$
- $J_{\mathrm{valid}}(a) = \{J_1{=}\{e_1,e_2,e_3\},\; J_2{=}\{p_1,p_2\},\; J_3{=}\{p_1\},\; J_4{=}\{g_1\}\}$

| Layer $\ell$ | $J \subseteq \mathrm{Comp}(\ell)$ | $C_{\min}^{\mathrm{ctrl},\ell}$ |
|---|---|---|
| exec | $J_1$ (size 3) | **3** |
| proto | $J_3$ (size 1) | **1** |
| gov | $J_4$ (size 1) | **1** |

Result: $C_{\min}^{\mathrm{ctrl,exec}} = 3 > C_{\min}^{\mathrm{ctrl,proto}} = 1$. Chain violated.

**Physical interpretation**: $J_1$ = 3-of-3 keeper committee (Chainlink OCR / Pyth
multi-publisher). $J_3 = \{p_1\}$ = single Pause Guardian. This is a real DeFi
configuration — execution-layer trust threshold exceeds protocol-layer threshold.
Inversion is structurally permitted, not pathological.

---

## 4. EL-1B-ctrl-cumulative theorem (correct replacement)

**Theorem EL-1B-ctrl-cumulative**:

Under L0 and cumulative layer definitions:

$$\boxed{C_{\min}^{\mathrm{ctrl},\leq\mathrm{gov}}(a) \leq C_{\min}^{\mathrm{ctrl},\leq\mathrm{proto}}(a) \leq C_{\min}^{\mathrm{ctrl},\leq\mathrm{exec}}(a)}$$

**Direction is reversed relative to EL-1B-break.**

**Proof**: By min-covering co-monotonicity (L2): $A \subseteq B \Rightarrow \min\mathrm{Cov}(B) \leq \min\mathrm{Cov}(A)$.
L0 gives $\mathcal{J}^{\leq\mathrm{exec}} \subseteq \mathcal{J}^{\leq\mathrm{proto}} \subseteq \mathcal{J}^{\leq\mathrm{gov}}$;
cumulative comp sets expand in the same direction. Apply L2. $\square$

**X1 numerical check**: $C_{\min}^{\mathrm{ctrl},\leq\mathrm{gov}} = 1 \leq C_{\min}^{\mathrm{ctrl},\leq\mathrm{proto}} = 1 \leq C_{\min}^{\mathrm{ctrl},\leq\mathrm{exec}} = 3$. $\checkmark$

---

## 5. Execution-layer dominance (conditional regime)

When the exec layer contains the lowest-cost path:

$$C_{\min}^{\mathrm{ctrl}}(a) = C_{\min}^{\mathrm{ctrl,exec}}(a)$$

This is not a universal theorem — it is the regime in which execution-layer
automation (AgentHub, oracle keepers) provides the minimum-cost unsafe path.
DeFi CAPO/AgentHub is the canonical instance:
$C_{\min}^{\mathrm{ctrl,exec}} = 1$ (AgentHub), $C_{\min}^{\mathrm{ctrl,proto}} = 2$ (Risk Steward 2/2).

Design implication: fix the execution pipeline, not the multisig threshold.

---

## 6. Superseded statements from v0.2

The following statement appeared in v0.2's summary line and is **hereby retracted**:

> *EL-1B: exec ≤ proto ≤ gov (control-plane cost).*

Correct replacement: see §3 (falsified by X1) and §4 (cumulative reverse chain).

The break/invalidation separation introduced in v0.2 is retained and correct.
The CAPO attribution correction (AgentHub, not Risk Steward) from v0.2 is retained.

---

*CRT Execution Layer Min-Cut Extension v0.3 — CLOSED.*
*Supersedes v0.2. EL-1B-break holds; EL-1B-ctrl single-layer chain false (X1); cumulative ctrl reverse chain holds.*
