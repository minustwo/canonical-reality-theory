# CRT Bridge Hardening Index v1.1

**Date**: 2026-04-29
**Status**: CURRENT
**Purpose**: Single source of truth for all closed/sealed CRT proof documents.

> **Erratum (2026-04-29)**: Block 3 EL-1B entry below has been corrected.
> The single-layer ctrl chain was falsified by counterexample X1.
> See `CRT_EXECUTION_LAYER_MINCUT_v0_3.md` for the corrected theorem split.

---

## Block 1: Core Bridge Theory

| Document | Version | Status | Commit | Content |
|---|---|---|---|---|
| `CRT_BRIDGE_THEOREM_FINAL_v1_0.md` | v1.0.1 | **SEALED** | `c09d0e06` | Weak Bridge: TracedSCSet ⊆ UnbreakSet ⊆ SCSet under C1+C2+C5_R |
| `CRT_BRIDGE_HIERARCHY_v0_1.md` | v0.3 | **CLOSED** | `31a977e5` | Full Bridge: SCSet = UnbreakSet = TracedSCSet under C1+C2+C5_R+C6 |
| `CRT_CONDITION_INDEPENDENCE_v0_1.md` | v0.2 | **CLOSED** | `344f61ab` | C1/C5_R/C6 each independently necessary |

**Proof chain:**
```
Weak Bridge (C1+C2+C5_R)
  → Full Bridge (+ C6): SCSet = UnbreakSet = TracedSCSet
  → Condition Independence: minimality of C1/C5_R/C6
```

---

## Block 2: Mixed / Finite Robustness

| Document | Version | Status | Commit |
|---|---|---|---|
| `CRT_MIXED_L2_ROBUSTNESS_v0_1.md` | v0.2 | **CLOSED** | `f9fa6a44` |

For Class III systems: $C_{\min}^{mix} \geq \theta$ (not $+\infty$).

---

## Block 3: Application / Control-Plane

| Document | Version | Status | Commit |
|---|---|---|---|
| `CRT_EXECUTION_LAYER_v0_1.md` | v0.2+erratum | **CLOSED** | `ecf4fa27` |
| `CRT_EXECUTION_LAYER_MINCUT_v0_3.md` | v0.3 | **CLOSED** | `2db6282c` |
| `DEFI_CRT_VERIFICATION_v0_1.md` | v0.4 | **CLOSED** | `cfc77b47` |

**EL-1B corrected theorem split (v0.3)**:

| Label | Statement | Status |
|---|---|---|
| EL-1B-break | $C_{\min}^{break,exec} \leq C_{\min}^{break,proto} \leq C_{\min}^{break,gov}$ | **Theorem** |
| EL-1B-ctrl-single | $C_{\min}^{ctrl,exec} \leq C_{\min}^{ctrl,proto} \leq C_{\min}^{ctrl,gov}$ | **False — X1 counterexample** |
| EL-1B-ctrl-cumulative | $C_{\min}^{ctrl,\leq gov} \leq C_{\min}^{ctrl,\leq proto} \leq C_{\min}^{ctrl,\leq exec}$ | **Theorem (direction reversed)** |

**Why the directions differ**: Break uses $\forall$+min-HS (anti-monotone in $\mathcal{J}^\ell$);
ctrl uses $\exists$+min-covering (co-monotone in $\mathrm{Comp}^{\leq\ell}$).
The v0.2/v1 error was applying the break-chain monotonicity argument to the ctrl chain.

**Canonical CAPO attribution**: zero-attacker realization of $C_{\min}^{ctrl,exec}=1$
at AgentHub (execution layer), not $C_{\min}^{ctrl,proto}=2$ at Risk Steward (protocol layer).

---

## Complete hardening chain

```
Bridge Final (SEALED) → Bridge Hierarchy (CLOSED) → Condition Independence (CLOSED)
  → Mixed L2 Robustness (CLOSED)
  → Execution Layer Min-Cut v0.3 (CLOSED) [supersedes v0.2]
  → DeFi CRT Verification (CLOSED)
```

Full source: `minustwo/market-structure-theory/papers/crt/`

---

*Index v1.1. Updated 2026-04-29: EL-1B ctrl-chain corrected.*
