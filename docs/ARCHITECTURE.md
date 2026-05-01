# Architecture
## Purpose
This document defines the public architecture of the MST–CRT–IET research stack.
It is an architecture map, not a theorem statement.
## Stack overview
```text
MST  →  CRT  →  IET

The stack should be read as layered dependency structure.

The layers should not be collapsed.

⸻

MST layer

MST is the structural canonicalization and admissibility layer.

It studies:

* interpretation spaces
* admissible worlds
* structural canonicality
* determinization
* completion operators
* structural plurality
* epistemic plurality
* Layer-1 canonicalization limits

Public status:

* MST v2.16.4 is treated as an ARCHIVAL Layer-1 core.
* It is not treated as a fully stratified final core.
* Establishing (4') does not automatically establish full property (4).

⸻

CRT layer

CRT is the bridge, escape-cost, robustness, and synthesis layer.

It studies:

* correctness / robustness alignment
* bridge conditions
* break paths
* C_min
* source-layer escape
* justification validity
* traceability
* robustness under structural pressure

Public status:

* Bridge results are conditional on explicit bridge conditions.
* Escape-cost interfaces are treated as separate CRT-layer objects.
* CRT should not be retroactively folded into MST Layer 1.

⸻

IET layer

IET refers to Inferential Equilibrium Theory.

It is the dynamic adoption and stochastic-selection layer.

It studies:

* adoption of canonical worlds
* stochastic stability
* process-specific convergence
* noisy best-response or related dynamic processes
* conditions under which canonical states may become selected

Public status:

* IET v2.3 is treated as conditional and process-specific.
* Claims involving unique P^{canon} depend on explicit MST conditions.
* IET is not a universal dynamic canonicality theorem.

⸻

Applications layer

Institutional, governance, market, DeFi, AI-system, and organizational interpretations belong to the application layer.

Applications may illustrate or instantiate the theory, but they do not prove the general stack.

Application material should live under:

applications/

unless it is explicitly formalized as MST, CRT, or IET development.

⸻

Dependency discipline

* MST is not CRT.
* CRT is not IET.
* Applications are not proofs of the stack.
* IET should not be used to prove MST or CRT claims.
* CRT bridge statements must remain conditional unless their assumptions are explicitly satisfied.
* Full synthesis claims require explicit dependency tracking.

⸻

Public repository role

This repository is a curated public research interface.

It tracks:

* architecture
* status
* proof maturity
* open problems
* release history
* AI-assisted research process

It is not a raw private research archive.

⸻
```
