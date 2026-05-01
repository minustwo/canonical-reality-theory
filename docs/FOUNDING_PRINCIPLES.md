# Founding Principles

## Status

Status: METHODOLOGY / ARCHITECTURE.

Peer review: Not externally peer reviewed.

AI assistance: This document is part of an AI-assisted research repository.

Claim-status impact: No theorem-status change.

Scope: Research-governance principles.

## Purpose

This document records the public-safe version of the founding principles that guided the development of the CRT research stack.

These principles are not theorem statements.

They are not proof artifacts.

They are not peer review.

They are research-governance constraints used to guide theory development, audit discipline, and public-release boundaries.

## Historical role

The founding principles were not introduced as a post-hoc justification for CRT.

They first appeared as constraints for an earlier market-description and execution-language problem.

They were later recognized as the constitutional layer under which the MST, IET, and CRT research stack developed.

This document records the principles as public-facing research-governance concepts, not as raw private history.

## Principle 1 — Objectivity

The research process should describe structures rather than construct convenient narratives.

Operational meaning:

- do not force a result to fit a preferred story
- preserve counterexamples
- distinguish observation from interpretation
- separate artifacts from rhetoric
- describe the structure before deciding what to do with it

Public-release implication:

```text
A public artifact should say what it establishes and what it does not establish.
```

## Principle 2 — Precision

The research process should avoid vague correctness.

Operational meaning:

* define status labels
* separate theorem, sketch, audit, and open problem
* state assumptions explicitly
* avoid hidden equivalence claims
* preserve dependency boundaries
* avoid treating approximate correctness as formal correctness

Public-release implication:

```text
A claim should be no stronger than its assumptions allow.
```

## Principle 3 — Honesty

The research process should expose errors rather than hide them.

Operational meaning:

* preserve audit trails
* mark superseded artifacts
* record corrections
* demote claims when needed
* do not erase uncertainty
* do not treat internal audit as peer review
* do not use public release to imply final completion

Public-release implication:

```text
Transparent correction is stronger than hidden revision.
```

## Principle 4 — Pure reasoning

The research process should distinguish deductive structure from empirical, institutional, or rhetorical validation.

Operational meaning:

* do not use examples as proofs
* do not use application success as theorem completion
* separate diagnostic artifacts from formal artifacts
* distinguish proof from plausibility
* separate structural claims from performance claims

Public-release implication:

```text
Applications may illustrate theory, but they do not automatically prove it.
```

## Principle 5 — Recursive completeness / closure discipline

The research process should track whether dependencies are internal, external, open, or discharged.

Operational meaning:

* identify unresolved assumptions
* record open dependencies
* freeze unresolved conflicts when necessary
* avoid pretending that local closure is global closure
* distinguish staged release from final completion
* preserve boundary conditions when moving across layers

Public-release implication:

```text
A closed artifact is closed only within its stated scope.
```

## How these principles shaped the repository

These principles help explain why this repository emphasizes:

* status labels
* claims ledgers
* proof-status sidecars
* open-problem records
* public correction
* legacy archive boundaries
* AI-agent role separation
* context-reset audit
* private / public separation
* staged public release summaries

## Non-claims

This document does not claim:

* CRT is correct
* MST is complete
* IET is complete
* full synthesis is proved
* the founding principles are mathematical axioms by themselves
* the founding principles are sufficient for theorem correctness
* AI-assisted audit is peer review
* public release is institutional validation
* repository history proves theorem correctness

## Relationship to other files

Read with:

* `docs/EMERGENT_RESEARCH_PROCESS.md`
* `docs/PROJECT_PROVENANCE.md`
* `docs/METHODOLOGY_RETROSPECTIVE_v0_1.md`
* `docs/RESEARCH_PROCESS.md`
* `docs/STATUS_LABELS.md`
* `docs/AUDIT_PROTOCOL.md`
* `docs/ADVERSARIAL_THEORY_DEVELOPMENT_PROTOCOL.md`

---

## END FILE
