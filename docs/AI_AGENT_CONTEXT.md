AI Agent Context Memo

Purpose

This memo records the operational context for AI agents working on this public repository.

It exists because the repository contains both:

1. a clean public research surface, and
2. legacy CRT technical / proof archive material.

Future AI agents should read this memo before proposing repository, architecture, or theory changes.

Repository identity

This repository is:

AI-assisted, versioned research repository
for the MST–CRT–IET architecture stack

It is not:

* a software product
* a normal paper repository
* a finalized monograph
* a finished theorem archive
* a raw private research dump

The repository uses software-style version control for research artifacts.

The objects under version control include:

* definitions
* theorem statements
* proof artifacts
* assumptions
* counterexamples
* audit records
* open problems
* dependency maps
* release notes

Current public-repo model

The public repository should be understood as a research operating system for the CRT stack.

The intended public surface is:

README.md
docs/ARCHITECTURE.md
docs/STATUS.md
docs/CLAIMS_LEDGER.md
docs/OPEN_PROBLEMS.md
docs/READING_GUIDE.md
docs/RESEARCH_PROCESS.md
docs/TERMINOLOGY.md

Layer entry points:

mst/
crt/
iet/
proofs/
applications/
releases/
archive/

Legacy material may still exist under older paths during migration.

Legacy paths should not be interpreted as final architecture unless the status files say so.

Historical layering issue

The current public repo has two historical layers:

Layer A — new clean research surface
Layer B — older CRT technical / proof archive surface

Do not assume the repo is empty or newly initialized.

Do not assume the clean surface is the whole repo.

Do not ignore legacy technical files such as:

* THEORY_INDEX.md
* PUBLICATION_STATUS.md
* STATUS_GLOSSARY.md
* papers/foundations/
* proofs/supplement/
* papers/open-systems/

MST current understanding

MST has two public-facing forms.

1. Archival / legacy foundation form

MST v2.16.4 should be treated as:

ARCHIVAL Layer-1 core
pre-stratified
not final stratified MST core

Known boundary:

(4') established
full property (4) not automatic
no automatic AC-6 promotion

Do not present MST v2.16.4 as a completed final stratified theory.

2. Decomposed public presentation

The papers/mst/ material is a decomposed determinization presentation.

It is useful for public explanation, but it should not be confused with the full historical MST core.

The next theoretical architecture task is not to keep expanding the paper draft.

The next theory task is:

MST_LANGUAGE_v0_1
MST_STRATIFIED_CORE_v0_1

but only after architecture scan and status unification.

CRT current understanding

CRT is not MST.

CRT is the bridge, escape-cost, robustness, and synthesis layer.

CRT includes:

* bridge hierarchy
* break paths
* source-layer escape
* C_min
* traceability
* correctness / robustness alignment
* synthesis dependencies

Bridge claims remain conditional unless all bridge assumptions are explicit.

C_min / escape interfaces should not be folded back into MST Layer 1.

CRT belongs to a separate layer above MST.

IET current understanding

IET should refer to:

Inferential Equilibrium Theory

IET is the dynamic adoption and stochastic-selection layer.

Known boundary:

IET v2.3 is process-specific and conditional.
Claims involving unique P^{canon} depend on explicit MST property (4) / MST-4 assumptions.
Reduced sliding-window results do not imply full dynamic canonicality.

There is a legacy naming conflict where IET was sometimes described as institutional / interpretive / invariant escape theory.

Going forward:

* IET should mean Inferential Equilibrium Theory.
* Institutional / governance / market / AI-system interpretations should be treated as application-layer material unless explicitly formalized.

Do not use IET to prove MST or CRT claims.

Sig0 / FDT current understanding

Sig0 / FDT artifacts should be treated as:

AUDIT / CONDITIONAL
sandbox-internal closure
with external dependencies

Do not present FDT as fully proved.

Do not restart FDT proof passes unless explicitly instructed.

Proof artifact policy

Proof artifacts may be public.

However:

public proof artifact ≠ global theorem completion
public audit ≠ theorem
internal audit ≠ peer review
Zenodo DOI ≠ peer review

Every major proof or audit artifact should eventually carry:

Status:
Peer review:
Review status:
AI assistance:
Citation status:
Scope:
Dependencies:
Known limitations:

Recommended proof categories:

proofs/closed/
proofs/conditional/
proofs/sketches/
proofs/audits/
proofs/superseded/
proofs/supplement/

Status labels

Use the canonical label family:

ARCHIVAL
SEALED
CLOSED
CONDITIONAL
SKETCH
AUDIT-ONLY
OPEN
SUPERSEDED
WORKING

Do not freely mix old and new labels without mapping them.

Avoid treating:

CLOSED = peer reviewed
SEALED = peer reviewed
PROVED = globally complete
ARCHIVAL = peer reviewed

These equivalences are false.

## Canonical status system
The canonical repository status-label reference is:
```text
docs/STATUS_LABELS.md
```

Future AI agents must treat this file as the source of truth for status labels.

The canonical labels are:

ARCHIVAL
SEALED
CLOSED
CONDITIONAL
SKETCH
AUDIT-ONLY
OPEN
SUPERSEDED
WORKING

Older files may use legacy or local labels such as:

PROVED
REVIEWED
PUBLIC-SAFE
PRIVATE-ONLY
DEPRECATED
DRAFT
SKETCHED
AUDIT-LOCAL
ACCEPTED diagnostic
Candidate theorem

These must be interpreted through docs/STATUS_LABELS.md.

Do not treat old labels as independent status systems.

Do not infer peer review from any internal label.

In particular:

SEALED ≠ peer reviewed
CLOSED ≠ peer reviewed
ARCHIVAL ≠ peer reviewed
PROVED ≠ globally complete
AUDIT-ONLY ≠ theorem
Zenodo DOI ≠ peer review
AI-assisted audit ≠ peer review

If there is a conflict between:

docs/STATUS.md
docs/CLAIM_LABELS.md
STATUS_GLOSSARY.md
THEORY_INDEX.md
PUBLICATION_STATUS.md

use:

docs/STATUS_LABELS.md

as the canonical status reference.

Current priority order

The current repo priority is:

1. Rebuild public research surface. DONE on branch `public-research-rebuild-v1`.
2. Add AI-agent context memo. DONE.
3. Unify status vocabulary. CURRENT.
4. Resolve IET naming conflict.
5. Add status headers to proof artifacts.
6. Reclassify legacy technical archive / `THEORY_INDEX.md`.
7. Add architecture deep-scan artifact.
8. Only then design `MST_LANGUAGE_v0_1` / `MST_STRATIFIED_CORE_v0_1`.

Current non-actions

Do not do the following unless explicitly instructed:

* Do not discuss arXiv submission strategy.
* Do not rewrite MST paper content.
* Do not expand CRT paper scaffolds.
* Do not start IET L6/L7.
* Do not restart Sig0 / FDT proof work.
* Do not claim Equivalence III proof completion.
* Do not write synthesis paper.
* Do not import private raw material.
* Do not promote conditional theorem statements.

Public reader safety

The repository should prevent the following misreadings:

* MST v2.16.4 proves full property (4) in general.
* ICT determinization reaches AC-6 unconditionally.
* CRT bridge is unconditional.
* C_min belongs inside MST Layer 1.
* IET proves full dynamic canonicality.
* Canonicality implies stochastic stability in full generality.
* Full MST–CRT–IET synthesis is already proved.
* AI-assisted audit equals peer review.
* Zenodo DOI equals peer review.

Default agent behavior

If uncertain:

1. preserve current status labels,
2. avoid theorem promotion,
3. avoid proof compression,
4. ask for human approval before public import,
5. make status boundaries more explicit,
6. do not silently merge layers.

⸻
