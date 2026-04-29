> **Erratum (2026-04-29)**: The "Refined layer ordering" in §3 is **incorrect**.
> The single-layer ctrl chain
> $C_{\min}^{ctrl,exec} \leq C_{\min}^{ctrl,proto} \leq C_{\min}^{ctrl,gov}$
> has been constructively falsified by counterexample X1 (validation report v4).
> The correct theorem split is in
> [`papers/robustness/CRT_EXECUTION_LAYER_MINCUT_v0_3.md`](../../papers/robustness/CRT_EXECUTION_LAYER_MINCUT_v0_3.md):
> - **EL-1B-break**: $C_{\min}^{break,exec} \leq C_{\min}^{break,proto} \leq C_{\min}^{break,gov}$ (holds)
> - **EL-1B-ctrl single-layer**: falsified by X1
> - **EL-1B-ctrl cumulative**: $C_{\min}^{ctrl,\leq gov} \leq C_{\min}^{ctrl,\leq proto} \leq C_{\min}^{ctrl,\leq exec}$ (holds, direction reversed)

# CRT Execution Layer — Min-Cut Extension v0.2

**Date**: 2026-04-28
**Status**: **CLOSED** (with erratum above)

**Changes from v0.1**:
1. Replaced source-count formulas with Break/min-HS layer-restricted machinery
2. Added empty-layer convention ($C_{\min}^\ell = +\infty$ when $\mathcal{J}^\ell = \emptyset$)
3. Separated two cut semantics: Break/invalidation vs capture/control
4. Reframed Risk Steward as $C_{\min}^{ctrl,proto} = 2$, not sealed break cost
5. Reframed CAPO as zero-attacker realization of execution-layer control cut
6. Defense/institution as threshold $C_{\min}^{exec} \geq \theta$

---

## 1. Two cut semantics

### Break/invalidation cut (sealed CRT machinery)

$$\mathcal{B}^\ell(a) := \{\mathrm{Break}(J) : J \in \mathcal{J}^\ell(a)\}$$
$$C_{\min}^{break,\ell}(a) := \min\text{-HS-cost}(\mathcal{B}^\ell(a))$$

Empty layer: $\mathcal{J}^\ell(a) = \emptyset \Rightarrow C_{\min}^{break,\ell}(a) = +\infty$.

### Control/capture cut (governance/pipeline semantics)

$$C_{\min}^{ctrl,\ell}(a) := \text{minimum components in layer }\ell\text{ to compromise for unsafe execution}$$

**Key distinction**: A 2/2 multisig has $C_{\min}^{break} = 1$ (disable either source) but $C_{\min}^{ctrl} = 2$ (must compromise both signers).

---

## 2. Three-layer decomposition

$$\mathcal{J}_{\mathrm{valid}}(a) = \mathcal{J}^{gov}(a) \cup \mathcal{J}^{proto}(a) \cup \mathcal{J}^{exec}(a)$$

| Layer | Examples |
|---|---|
| $\mathcal{J}^{gov}$ | AIP + timelock; DAO vote |
| $\mathcal{J}^{proto}$ | Risk Steward multisig; Pause Guardian |
| $\mathcal{J}^{exec}$ | AgentHub; oracle keepers; automated parameter updates |

---

## 3. Theorems

**EL-1A** (Break/invalidation three-layer min):
$$C_{\min}^{break}(a) = \min_{\ell \in \{gov, proto, exec\}} C_{\min}^{break,\ell}(a)$$

**EL-1B** (Control/capture three-layer min):
$$C_{\min}^{ctrl}(a) = \min_{\ell \in \{gov, proto, exec\}} C_{\min}^{ctrl,\ell}(a)$$

**Refined layer ordering** *(RETRACTED — see Erratum at top)*:
~~$C_{\min}^{ctrl,exec} \leq C_{\min}^{ctrl,proto} \leq C_{\min}^{ctrl,gov}$~~

See v0.3 for the corrected theorem split.

---

## 4. Aave CAPO formal mapping

| Cut type | gov | proto | exec | min |
|---|---|---|---|---|
| $C_{\min}^{break}$ | 1 | 1 | 1 | **1** |
| $C_{\min}^{ctrl}$ | 3–6 | 2 (Risk Steward 2/2) | **1** (AgentHub) | **1** |

$$\boxed{\text{CAPO: zero-attacker realization of a one-component execution-layer control cut.}}$$
$$C_{\min}^{ctrl,exec} = 1, \quad C_{\min}^{ctrl,proto} = 2$$

**Audit correction**: $C_{\min}(\text{Aave a1}) = 1$ is numerically correct but was misattributed to Risk Steward (protocol layer). Correct attribution: AgentHub execution layer. Redesign implication: fix the execution pipeline, not the multisig threshold.

---

## 5. Layer-identification protocol

For any safety property $a$:
1. Enumerate $\mathcal{J}^{gov}$, $\mathcal{J}^{proto}$, $\mathcal{J}^{exec}$
2. Compute $C_{\min}^{break,\ell}$ and $C_{\min}^{ctrl,\ell}$ per layer
3. Identify dominant layer: $\mathrm{argmin}_\ell C_{\min}^{ctrl,\ell}(a)$
4. Report $C_{\min}$ with layer attribution — not just the number

---

*CRT Execution Layer Min-Cut Extension v0.2 — CLOSED (with erratum).*
*Refined layer ordering retracted. See v0.3 for corrected theorems.*
