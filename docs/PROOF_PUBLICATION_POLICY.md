# Proof Publication Policy
## Purpose
This document defines how proof artifacts may be published in the public CRT research repository.
The guiding principle is:
```text
Proof artifacts may be public, but public proof artifacts must not be presented as proof of the full MST–CRT–IET synthesis.

Repository position

This repository is a public AI-assisted research repository.

It may contain:

* theorem statements
* proof drafts
* proof sketches
* audit notes
* counterexamples
* dependency analyses
* archived proof supplements
* superseded proof artifacts

Unless explicitly stated otherwise, these materials have not undergone formal external peer review.

Public proof principle

Proof artifacts may be public when their maturity status is explicit.

Allowed public forms include:

* SEALED
* CLOSED
* CONDITIONAL
* SKETCH
* AUDIT-ONLY
* SUPERSEDED
* OPEN
* WORKING

A proof artifact being public does not imply:

* global theorem completion
* unconditional synthesis
* peer review
* correctness across all domains
* discharge of unstated assumptions

Proof directory taxonomy

The recommended proof taxonomy is:

proofs/
  closed/
  conditional/
  sketches/
  audits/
  superseded/
  supplement/

proofs/closed/

For artifacts closed within a stated scope.

Citation boundary:

May be cited within stated scope.
Does not imply external peer review.
Does not imply global synthesis.

proofs/conditional/

For conditional theorems or proof artifacts whose assumptions remain active.

Citation boundary:

May be cited only with assumptions.
Do not cite as unconditional theorem.

proofs/sketches/

For proof sketches, coherent outlines, or partial derivations.

Citation boundary:

Do not cite as complete proof.

proofs/audits/

For audit notes, counterexamples, dependency audits, independence analyses, and adversarial review records.

Citation boundary:

May be cited as audit material.
Do not cite as theorem statement.

proofs/superseded/

For historical artifacts replaced by newer versions or corrected statements.

Citation boundary:

Do not cite as current.
Use only for provenance.

proofs/supplement/

For public proof supplements associated with papers, preprints, technical reports, or archival records.

Citation boundary:

Cite with supplement status.
Do not cite as peer-reviewed unless explicitly peer-reviewed.

Required artifact status block

Major proof artifacts should eventually include or be associated with:

Status:
Peer review:
Review status:
AI assistance:
Citation status:
Scope:
Dependencies:
Known limitations:

Sidecar status ledgers may be used before inline headers are added.

Peer-review boundary

The following are not peer review:

* internal audit
* AI-assisted review
* adversarial language-model review
* Zenodo archival upload
* DOI assignment
* GitHub publication
* arXiv or SSRN availability

Only explicit acceptance by a recognized peer-reviewed venue should be described as peer review.

AI-assistance boundary

AI systems may assist with:

* drafting
* refactoring
* proof-status bookkeeping
* adversarial review
* repository maintenance
* cross-document consistency checks

AI assistance is not proof certification.

AI-assisted audit is not peer review.

Human maintainers remain responsible for public release decisions.

Misreadings to prevent

Public proof releases must prevent the following misreadings:

MST misreading

Wrong:

MST proves AC-6 for ICT unconditionally.

Correct boundary:

MST v2.16.4 is archival Layer-1 core material; `(4')` does not automatically imply full `(4)` or AC-6.

IET misreading

Wrong:

IET proves canonicality iff stability in full generality.

Correct boundary:

IET v2.3 is process-specific and conditional; results involving unique P^{canon} require explicit MST assumptions.

FDT misreading

Wrong:

FDT is fully proved.

Correct boundary:

FDT-related artifacts should be treated as audit / conditional unless external dependencies are discharged.

Synthesis misreading

Wrong:

The full MST–CRT–IET synthesis is proved unconditionally.

Correct boundary:

The public repository records a conditional theorem landscape, not unconditional synthesis.

Release rule

A proof release must state:

Version:
Release type:
Status:
Peer review:
AI assistance:
Scope:
Dependencies:
Citation status:
Known limitations:
Claim-status impact:

Default rule

If the proof status is uncertain, use the weaker label.

Do not silently promote proof maturity.

⸻
