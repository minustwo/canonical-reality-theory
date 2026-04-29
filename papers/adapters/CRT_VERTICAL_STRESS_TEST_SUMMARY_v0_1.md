# CRT Vertical Stress Test Summary

**Version**: 0.1
**Date**: 2026-04-29

**Status**: ACCEPTED diagnostic artifact.
**Publication status**: Technical-report / research-archive material. Not peer-reviewed.
**Scope**: Four vertical stress-test suites: boundary precision, quantum extension,
adapter stability, and complexity. Not a sealed theorem file.

> These suites test the depth and stability of CRT's adapter framework
> rather than its breadth across languages. All 30 cuts produced no unexpected failures.

---

## Overview

| Suite | Cuts | PASS | EXPECTED BOUNDARY | Main result |
|---|---|---|---|---|
| CJC Boundary | 7 | 4 | 3 | R0c $\perp$ CJC; CJC candidate theorem |
| QNL Boundary | 8 | 5 | 3 | Bell's theorem confirms QNL structural |
| Adapter Stability | 7 | 3 | 4 | Composition min-cut law; Class I→III degradation |
| Complexity | 8 | 7 | 1 | LocalExplain poly-verify $\neq$ $C_{\min}$ NP-hard |
| **Total** | **30** | **19** | **11** | **0 unexpected failures** |

---

## Suite 1: CJC Boundary

**CJC — Circular Justification Consistency** is a new classical justification
boundary discovered during the 16-language stress tests and formalized here.

**Definition**: A justification system has CJC if justification validity depends
on the global extension / accepted-justification set that is itself determined
by which justifications are accepted. No local certificate can be assigned
without solving the whole extension first.

**Key result — R0c $\perp$ CJC** (CJC-7):
A system can pass R0c (bounded absence is certifiable) and still fail CJC
(circular adoption invalidation). These are independent conditions.

The NAA Reformulation Theorem v0.2 applies only to the absence-premise
component (R0c). CJC is an independent obstruction that NAA reformulation
does not remove.

**CJC avoidance** (three sufficient conditions):
1. Normal defaults with acyclic dependency graph
2. Stratification (each layer references only lower-layer results)
3. Total priority ordering (conflicts resolved without global extension knowledge)

**Status**: CJC is a new classical boundary class. The avoidance conditions
are verified diagnostically; formal proof within CRT's axioms is an open question.

| Cut | Result |
|---|---|
| CJC-1: Acyclic normal defaults | PASS |
| CJC-2: Mutual default cycle | EXPECTED BOUNDARY (CJC) |
| CJC-3: Autoepistemic self-supporting belief | EXPECTED BOUNDARY (CJC) |
| CJC-4: Defeasible logic with priority | PASS |
| CJC-5: Stratified default chain | PASS |
| CJC-6: Odd cycle — no stable extension | EXPECTED BOUNDARY (world loss) |
| CJC-7: Bounded absence + circular adoption | EXPECTED BOUNDARY (CJC) — confirms R0c $\perp$ CJC |

---

## Suite 2: QNL Boundary

**QNL — Quantum Non-Locality** is an extension boundary for CRT.

Current CRT is **classical/local support-graph CRT**:
$$B_T \cap \mathrm{At}_T = \emptyset, \qquad J \subseteq N_T \times \mathrm{At}_T$$

Every edge in a justification $J$ connects a local source node to a local
atom target. This model is appropriate for classical systems.

**Bell's theorem** (QNL-4) establishes that quantum entanglement cannot be
represented by any local hidden variable model. CRT's source-node model
is an LHV model. Therefore QNL is a **structural boundary**, not an
empirical limitation.

**QNL is not an unexpected failure of CRT core.** Classical CRT remains
fully valid for all 15 other tested domains. Post-measurement quantum
systems recover classical CRT fully (measurement collapses the quantum
state to a definite classical world).

**Four extension requirements** for a quantum-CRT:
- QNL-E1: Complex-amplitude admissibility (including interference)
- QNL-E2: Non-local source nodes
- QNL-E3: Non-duplicable justifications (no-cloning)
- QNL-E4: $\mathrm{EV}_Q$ — quantum validity operator analogous to $\mathrm{EV}_C$, not identical

| Cut | Result |
|---|---|
| QNL-1: Classical probabilistic mixture | PASS |
| QNL-2: Product-state quantum circuit | PASS |
| QNL-3: Entangled Bell pair | EXPECTED BOUNDARY (QNL) |
| QNL-4: Bell inequality violation | EXPECTED BOUNDARY (QNL — Bell's theorem) |
| QNL-5: No-cloning | EXPECTED BOUNDARY (QNL + C1) |
| QNL-6: Measurement = $\mathrm{EV}_Q$ analog | PASS |
| QNL-7: Error correction = Institution Layer 6 | PASS |
| QNL-8: Extension spec | Extension boundary characterized |

---

## Suite 3: Adapter Stability

This suite tests whether CRT adapters give consistent results when the same
system is viewed differently: different representation, projection, composition,
evidence refinement, or execution-layer insertion.

**Main results**:

**Result 1 — Projection (source-merge pattern)**:
In cases where coarse-graining merges source nodes that are actually shared,
projection can overestimate $C_{\min}$ by hiding the shared source.
Robustness analysis must be done at the finest granularity.
Note: this is not a universal law for all projections; it applies to
the source-merge / shared-source hiding pattern specifically.

**Result 2 — Composition min-cut law (control/execution cuts)**:
$$C_{\min}^{\mathrm{ctrl},A\circ B} \leq \min(C_{\min}^{\mathrm{ctrl},A},\ C_{\min}^{\mathrm{ctrl},B})$$
The weakest control path dominates the composed system. This generalizes
the Execution Layer EL-1B result to arbitrary composition.

For break/invalidation costs ($C_{\min}^{\mathrm{break}}$): an analogous
inequality holds at the break-family level, but only under layer-separable
assumptions. Without layer separation, the composed break-family must be
analyzed directly.

**Result 3 — Execution insertion = CRT-SEI O2b**:
Inserting an execution layer adds a new source node to $B_T$ (O2b event).
The existing adapter's $C_{\min}^{\mathrm{ctrl}}$ is stale and must be recomputed.
DeFi CAPO/AgentHub is the canonical application instance.

**Result 4 — Class I → Class III degradation**:
A Class I system (e.g., Datalog, LocalExplain holds) whose output is consumed
by a Class III system (LLM) produces a Class III composed system.
LocalExplain is lost; $C_{\min}$ gains new hallucination attack vectors.

| Cut | Result |
|---|---|
| STAB-1: Translation Datalog ↔ SQL recursive | PASS (CWA caveat) |
| STAB-2: Projection — source-merge overestimate | EXPECTED BOUNDARY |
| STAB-3: Composition — $C_{\min}^{\mathrm{ctrl}}$ min-cut | PASS (non-additive) |
| STAB-4: Evidence refinement | PASS / EXPECTED BOUNDARY |
| STAB-5: Execution insertion | EXPECTED BOUNDARY |
| STAB-6: Symmetry — not equivariant in general | EXPECTED BOUNDARY |
| STAB-7: Class I → Class III under LLM | PASS (degradation expected) |

---

## Suite 4: Complexity Stress Tests

This suite tests the computational complexity of key CRT adapter operations.

**Main result — LocalExplain vs $C_{\min}$ complexity gap**:
$$\text{LocalExplain: poly-time verifiable} \quad \neq \quad C_{\min}: \text{NP-hard to compute (general)}$$

LocalExplain requires existence and verifiability of certificates, not
efficient computability. NP-hardness of finding a justification does not
violate LocalExplain if verification is polynomial.

**DAG / network-cut tractability**:
When the attack graph has network-cut / DAG structure (e.g., DeFi governance
and execution layers), $C_{\min}^{\mathrm{ctrl}}$ reduces to max-flow / min-cut
and is polynomial. General break/min-HS instances on the same DAG may retain
NP-hardness (MWHS formulation). Structure determines tractability.

**LP dual as poly-time lower bound**:
For integer-structured attack problems (CSP/MIP), LP relaxation dual provides
a polynomial-time computable lower bound on $C_{\min}$.

**CJC detection complexity**:
Detecting CJC in general default logic is $\Sigma_2^P$-hard. Under CJC-avoidance
designs (normal + acyclic, stratified, priority-ordered), detection is polynomial.

| Domain | LocalExplain complexity | $C_{\min}$ complexity |
|---|---|---|
| Datalog | Polynomial | NP-hard (MWHS); approx $O(\log n)$ |
| SQL provenance | Polynomial | NP-hard; $\#P$-hard (full enumeration) |
| CSP / MIP | Polynomial | NP-hard; LP dual = poly lower bound |
| Type theory | Polynomial (verify) | PSPACE (proof search) |
| DeFi | Polynomial | Poly ($C_{\min}^{\mathrm{ctrl}}$ via max-flow on DAG) |
| LLM | Polynomial ($k$ verifiers) | NP-hard; $O(\log n)$ approx |
| Temporal logic | Polynomial | NP-hard / poly (network-cut safety) |
| CJC detection | Poly (special cases) | $\Sigma_2^P$ (general default logic) |

---

## Cross-suite findings

**Boundary taxonomy composability** (from Boundary Interaction Suite):
All seven boundary types (C1, R0c, Type S, Fork B, Execution-cut, CJC, QNL)
compose without misclassification:
- R0c $\perp$ CJC (CJC-7)
- Type S $\perp$ C6
- Fork B $\Rightarrow$ C6 failure (structural link)
- break $\perp$ ctrl dimensions

**Regression baseline** (from Regression Consistency Suite):
All sealed/closed CRT theorem files are mutually consistent as of 2026-04-29.
Two citation watch items: (1) "C5" in Representation Theorem = ULift-sat route,
not C5_R primitive; (2) "Full adapter fit" $\neq$ Full Bridge theorem.

---

## Open questions (selected)

| OQ | Question |
|---|---|
| CJC-OQ-1 | Is the CJC candidate theorem provable within CRT's sealed axioms? |
| QNL-OQ-1 | Are QNL-E1/E2/E3/E4 a minimal extension set? |
| STAB-OQ-2 | Can the composition min-cut law be tightened to equality under specific conditions? |
| COMP-OQ-1 | Is there a poly-time exact $C_{\min}^{\mathrm{break}}$ algorithm for tree-structured justification families? |

---

*CRT Vertical Stress Test Summary v0.1. 2026-04-29.*
*ACCEPTED diagnostic artifact. Not a sealed theorem file. Not peer-reviewed.*
*Suites: CJC Boundary (7 cuts) + QNL Boundary (8 cuts) + Adapter Stability (7 cuts) + Complexity (8 cuts) = 30 cuts total.*
