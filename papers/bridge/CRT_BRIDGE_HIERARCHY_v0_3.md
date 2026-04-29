> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: CLOSED. See [STATUS_GLOSSARY.md](../../STATUS_GLOSSARY.md).

# CRT Bridge Hierarchy — v0.3

**Date**: 2026-04-28 | **Status**: CLOSED

## Overview

| Level | Statement | Conditions |
|---|---|---|
| **Weak Bridge** | TracedSCSet ⊆ UnbreakSet ⊆ SCSet | C1+C2 (left), C5_R (right) |
| **Full Bridge** | SCSet = UnbreakSet = TracedSCSet | C1+C2+C5_R+C6 |
| *CertReach characterization* | UnbreakSet = SCSet ∩ CertReach | Corollary of Full Bridge |

## Primitive conditions

| Condition | Name | Content |
|---|---|---|
| C1 | LocalExplain | Cert$_i$ satisfying R0a–R0e |
| C2 | DeclCompat | $J^{int} \in \mathcal{J}_{\mathrm{declared}}$ |
| C5_R | RightBridge | UnbreakSet ⊆ SCSet |
| C6 | TraceComplete | SCSet ⊆ CertReach |

**C3 (NDLift) and C4 (DeclComplete) are not primitive Bridge conditions.**
They belong to the sufficient construction route to C5_R:
$$\mathrm{C1} \wedge \mathrm{C3} \wedge \mathrm{C4} \Rightarrow \mathrm{ULift\text{-}sat} \Rightarrow \mathrm{C5_R}$$

## Weak Bridge (Sealed)

$$\mathrm{TracedSCSet}_T(\Pi) \subseteq_{\mathrm{C1+C2}} \mathrm{UnbreakSet}_T(\Pi) \subseteq_{\mathrm{C5_R}} \mathrm{SCSet}_T(\Pi)$$

## Full Bridge

Under C1+C2+C5_R+C6: $\mathrm{SCSet} = \mathrm{UnbreakSet} = \mathrm{TracedSCSet}$.

C6 sufficient: exact evidence (CWA) + pure rule-generated $\mathcal{F}$. Not automatic for Fork B.

## CertReach characterization

Under C1+C2+C5_R+C6: $\mathrm{UnbreakSet} = \mathrm{SCSet} \cap \mathrm{CertReach}$.

Proof chain: UnbreakSet $\to^{\mathrm{C5_R}}$ SCSet $\to^{\mathrm{C6}}$ CertReach. C3 not used at primitive level.

## Counterexamples

**CE-1 (Full Bridge fails without C6)**: ICT Fork B, non-trivial $\Pi$.
$P_{\mathrm{wit}} \in \mathrm{SCSet} \setminus \mathrm{TracedSCSet}$. Tier-3 atoms block CertReach.

**CE-2 (C5_R fails without C3)**: Phantom source-free $J^{ph}$ inflates UnbreakSet.
$\{a^*\} \in \mathrm{UnbreakSet} \setminus \mathrm{SCSet}$.

## Minimality

C1/C5_R/C6: formally proved. C2: sketched (B-OQ-1 open).

## ICT + CWA

Satisfies C1+C2+C5_R but NOT C6 (Tier-3 Fork B atoms). Weak Bridge witness only.
Full Bridge requires internally grounded theory (Fork A / Class I/II).

**Open**: B-OQ-3 — Full Bridge witness with $|\mathrm{SCSet}| > 1$?

*End of CRT Bridge Hierarchy v0.3 — CLOSED.*
