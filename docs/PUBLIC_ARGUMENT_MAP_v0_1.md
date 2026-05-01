# Public Argument Map v0.1

## Status

Artifact type: Public argument map.

Status: CONDITIONAL / WORKING.

Peer review: Not externally peer reviewed.

AI assistance: This document is part of an AI-assisted research repository.

Claim-status impact: No theorem-status change.

Scope: Public-readable argument path for the MST–CRT–IET stack.

## Purpose

This document explains the current public argument path of the CRT research stack.

It is intended to help readers understand how the public artifacts relate to one another.

It is not:

- a theorem statement
- a proof artifact
- a peer-reviewed publication
- a full synthesis proof
- a mirror of private R&D material
- a substitute for the Zenodo records
- a substitute for proof-status ledgers

## Public argument path

The current public argument path is:

```text
MST
  -> CRT
  -> IET
```

In words:

```text
structural admissibility and determinization
  -> bridge, robustness, breakability, and escape-cost reasoning
  -> dynamic adoption and stochastic-selection questions under assumptions
```

This path is conditional.

It should not be read as an unconditional proof that the full MST–CRT–IET synthesis is complete.

## Layer 1 — MST

MST is the structural canonicalization and admissibility layer.

Public role:

* define interpretation spaces
* study admissible interpretation families
* analyze plurality
* formulate determinization
* study closure / comparability / joint-admissibility conditions
* expose the limits of Layer-1 canonicality

Current public artifact:

* Zenodo record `19937666`
* `artifacts/zenodo/19937666/STATUS.md`
* `mst/arguments/MST_PUBLIC_ARGUMENT_v0_1.md`

Current status:

```text
ARCHIVAL / CONDITIONAL
```

Boundary:

```text
MST v2.16.4 is treated as a pre-stratified Layer-1 core.
It does not automatically establish full property (4).
It does not automatically establish AC-6.
It is not the final stratified MST core.
```

## Layer 2 — CRT

CRT is the bridge, escape-cost, robustness, and synthesis layer.

Public role:

* relate structural correctness to robustness
* track break paths and source-layer escape
* define or use `C_min`-style reasoning
* study bridge conditions
* distinguish conditional alignment from unconditional equivalence

Current public artifacts:

* Zenodo record `19884063`
* `artifacts/zenodo/19884063/STATUS.md`
* `crt/arguments/CRT_PUBLIC_ARGUMENT_v0_1.md`
* `proofs/STATUS.md`
* `proofs/supplement/STATUS.md`

Current status:

```text
ARCHIVAL / CONDITIONAL
```

Boundary:

```text
CRT does not claim unconditional full synthesis.
Bridge claims require explicit assumptions.
Escape-cost and break-path reasoning should not be folded back into MST Layer 1.
```

## Layer 3 — IET

IET means Inferential Equilibrium Theory.

IET is the dynamic adoption and stochastic-selection layer.

Public role:

* ask whether canonical structures become selected
* study process-specific adoption
* relate dynamic stability to explicit MST / CRT assumptions
* expose the gap between structural canonicality and actual adoption

Current public artifact:

* `iet/arguments/IET_PUBLIC_ARGUMENT_v0_1.md`
* `docs/IET_NAMING.md`
* `proofs/supplement/STATUS.md`

Current status:

```text
CONDITIONAL / WORKING
```

Boundary:

```text
IET does not prove MST.
IET does not prove CRT.
IET does not establish full dynamic canonicality.
Claims involving unique canonical states depend on explicit assumptions.
```

## Why the argument path is staged

The public argument path is staged because each layer answers a different obstruction.

MST asks:

```text
What is structurally admissible?
```

CRT asks:

```text
What preserves or breaks structural correctness?
```

IET asks:

```text
Under what dynamics might a canonical structure be selected?
```

These are connected questions, but they are not automatically equivalent.

## Relationship to Zenodo records

Zenodo records are staged public research summaries.

They freeze citable states of the research program.

They do not constitute:

* peer review
* institutional endorsement
* final theorem completion
* full private R&D disclosure

Registered records:

* `artifacts/zenodo/19884063/`
* `artifacts/zenodo/19937666/`

## Relationship to private R&D

Private repositories remain the R&D, memory, and raw work layer.

This public repository is the release and interpretation layer.

The public argument map does not expose the full private R&D workspace.

## Non-claims

This document does not claim:

* full MST property (4)
* automatic AC-6
* unconditional CRT bridge
* full IET dynamic canonicality
* full correctness / robustness / stability equivalence
* peer review
* final theorem completion
* institutional endorsement

## Reading order

Recommended reading order:

1. `docs/PUBLIC_ARGUMENT_MAP_v0_1.md`
2. `mst/arguments/MST_PUBLIC_ARGUMENT_v0_1.md`
3. `crt/arguments/CRT_PUBLIC_ARGUMENT_v0_1.md`
4. `iet/arguments/IET_PUBLIC_ARGUMENT_v0_1.md`
5. `docs/CLAIMS_LEDGER.md`
6. `docs/OPEN_PROBLEMS.md`

---

## END FILE
