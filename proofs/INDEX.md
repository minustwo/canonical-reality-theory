# CRT Bridge Hardening Index v1.0

**Date**: 2026-04-29
**Status**: CURRENT
**Purpose**: Single source of truth for all closed/sealed CRT proof documents.

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
| `CRT_EXECUTION_LAYER_v0_1.md` | v0.2 | **CLOSED** | `ecf4fa27` |
| `DEFI_CRT_VERIFICATION_v0_1.md` | v0.4 | **CLOSED** | `cfc77b47` |

**Key result (EL-1B)**:
$$C_{\min}^{ctrl,exec} \leq C_{\min}^{ctrl,proto} \leq C_{\min}^{ctrl,gov}$$

Proof: $\mathcal{J}^{exec} \subseteq \mathcal{J}^{proto} \subseteq \mathcal{J}^{gov}$ + min-HS monotonicity. Four lines.

**Canonical CAPO attribution**: zero-attacker realization of $C_{\min}^{ctrl,exec}=1$ at AgentHub (execution layer), not $C_{\min}^{ctrl,proto}=2$ at Risk Steward (protocol layer).

---

## Complete hardening chain

```
Bridge Final (SEALED) → Bridge Hierarchy (CLOSED) → Condition Independence (CLOSED)
  → Mixed L2 Robustness (CLOSED)
  → Execution Layer Min-Cut (CLOSED)
  → DeFi CRT Verification (CLOSED)
```

Full source: `minustwo/market-structure-theory/papers/crt/`
