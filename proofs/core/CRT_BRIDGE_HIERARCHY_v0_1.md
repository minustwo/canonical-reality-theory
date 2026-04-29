# CRT Bridge Hierarchy — v0.3

**Date**: 2026-04-28
**Status**: **CLOSED**

**Changes from v0.2**:
1. C5 redefined as C5_R (direct right-bridge primitive: UnbreakSet ⊆ SCSet)
2. Strong Bridge demoted to CertReach characterization corollary
3. C3/C4 moved into "sufficient route to C5_R"

---

## 1. Overview

| Level | Statement | Conditions |
|---|---|---|
| **Weak Bridge** | TracedSCSet ⊆ UnbreakSet ⊆ SCSet | C1+C2 (left), C5_R (right) |
| **Full Bridge** | SCSet = UnbreakSet = TracedSCSet | C1+C2+C5_R+C6 |
| *CertReach characterization* | UnbreakSet = SCSet ∩ CertReach | corollary of Full Bridge under C6 |

---

## 2. Conditions

| Condition | Name | Content |
|---|---|---|
| C1 | LocalExplain | Certificate scheme $\mathrm{Cert}_i$ satisfying R0a–R0e |
| C2 | DeclCompat | Compiled $J^{int}$ enters $\mathcal{J}_{\mathrm{declared}}$ |
| C5_R | RightBridge | $\mathrm{UnbreakSet}_T(\Pi) \subseteq \mathrm{SCSet}_T(\Pi)$ |
| C6 | TraceComplete | $\mathrm{SCSet} \subseteq \mathrm{CertReach}$ (GlobalCoverage) |

Sufficient route to C5_R: $\mathrm{LocalExplain} \wedge \mathrm{NDLift} \wedge \mathrm{DeclComplete} \Rightarrow \mathrm{ULift}^{sat} \Rightarrow C5_R$.

---

## 3. Weak Bridge (SEALED v1.0.1)

**Theorem WB**: Under C1, C2, C5_R:
$$\mathrm{TracedSCSet}_T(\Pi) \subseteq_{C1+C2} \mathrm{UnbreakSet}_T(\Pi) \subseteq_{C5_R} \mathrm{SCSet}_T(\Pi)$$

---

## 4. Full Bridge

**Theorem FB**: Under C1, C2, C5_R, C6:
$$\mathrm{SCSet}_T(\Pi) = \mathrm{UnbreakSet}_T(\Pi) = \mathrm{TracedSCSet}_T(\Pi)$$

**Proof**: By C6: SCSet = TracedSCSet. By Weak Bridge: TracedSCSet ⊆ UnbreakSet ⊆ SCSet. Equalities collapse.

**Corollary** (CertReach characterization): Under C1+C2+C5_R+C6:
$$\mathrm{UnbreakSet}_T(\Pi) = \mathrm{SCSet}_T(\Pi) \cap \mathrm{CertReach}_T(\Pi)$$

---

## 5. Failure boundary

**CE-Bridge-1** (Full Bridge fails without C6): $T_{\mathrm{ICT}}^{v2.1}$, Fork B — Tier-3 atom `imbalance` is $B_T$-source-only → not in CertReach → not in TracedSCSet, yet in SCSet.

**CE-Bridge-2** (C5_R fails without NDLift): Phantom $J^{ph}$ with $\mathrm{Src}(J^{ph}) = \emptyset$ inflates UnbreakSet past SCSet.

---

## 6. Minimality

| Condition | Status |
|---|---|
| C1 | ✅ proved (black-box operator witness) |
| C2 | ⚠️ sketched (B-OQ-1) |
| C5_R | ✅ proved (CE-Bridge-2) |
| C6 | ✅ proved (CE-Bridge-1) |

---

*End of CRT Bridge Hierarchy v0.3 — CLOSED.*
