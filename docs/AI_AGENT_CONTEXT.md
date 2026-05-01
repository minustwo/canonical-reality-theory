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

Authorship, independence, and privacy boundary

The repository is an independent personal research project.

Canonical public handle:

minustwo

Future AI agents must preserve the maintainer’s privacy preference.

Do not add personal identifiers beyond the GitHub handle minustwo unless explicitly instructed.

Formal citation metadata may separately identify scholarly authorship in files such as:

CITATION.cff
Zenodo DOI records
formal manuscripts

General repository documentation should avoid unnecessary duplication of personal identity.

No claim in this repository should be interpreted as representing any university, employer, publisher, conference, journal, AI provider, research institute, company, or other institution unless explicitly stated.

AI assistance does not confer:

authorship authority
institutional endorsement
peer-review status
mathematical correctness

Human maintainers remain responsible for public release decisions and public claim boundaries.

Read:

docs/AUTHORSHIP_AND_PRIVACY.md

Execution and adversarial audit protocols

The repository now defines explicit execution and role protocols:

CODEX_WORKFLOW.md
docs/ROLE_MODEL.md
docs/ADVERSARIAL_THEORY_DEVELOPMENT_PROTOCOL.md
docs/AUDIT_PROTOCOL.md

Future AI agents must read these before proposing execution, audit, role, or methodology changes.

Role model summary:

Human maintainer = final authority
ChatGPT = architecture / control layer
Claude = auditor by default; producer only under explicit mode switch
Codex = repository execution agent
Perplexity = independent-style generator / cross-checker

Codex must be treated as:

repository execution agent
not theorem authority
not proof certifier
not peer reviewer

The repository uses three audit modes:

iterative adversarial audit
adversarial generation
context-reset audit

Context-reset audit is important for reducing shared-context bias.

However:

context-reset audit ≠ peer review
AI-assisted audit ≠ peer review
internal audit ≠ peer review

Every non-trivial Codex prompt should include:

main repository change
AGENTS.md / docs/AI_AGENT_CONTEXT.md update when relevant
verification that no theorem/proof files were modified
remote HEAD report after push

Methodology retrospective

The controlled methodology retrospective is:

docs/METHODOLOGY_RETROSPECTIVE_v0_1.md

This file records process lessons from AI-assisted CRT research development.

It should be interpreted as:

methodology / audit-only process artifact

It should not be interpreted as:

proof of theorem correctness
peer review
external validation
productivity benchmark
claim-status upgrade

Future AI agents must preserve this boundary.

The retrospective’s central process invariant is:

honesty over unsupported strength

When using the retrospective to design future workflows, do not turn process observations into theorem claims.

Methodology case study and development timeline

Controlled public process records:

docs/METHODOLOGY_CASE_STUDY_v0_1.md
docs/DEVELOPMENT_TIMELINE_v0_1.md

These files summarize internal methodology and development chronology in a public-safe way.

They should be interpreted as:

methodology / audit-only process artifacts

They should not be interpreted as:

theorem validation
peer review
external acceptance
productivity benchmark
institutional endorsement
claim-status upgrade

Future AI agents must not reproduce raw internal timeline reports verbatim.

Future AI agents must not add personal identifiers or private repository URLs.

Future AI agents must treat reported development metrics as internal historical context unless separately verified and public-safe.

Branch-level rebuild audit

The current branch-level rebuild audit is:

docs/REBUILD_AUDIT_v0_1.md

This audit checks whether public-research-rebuild-v1 coherently represents the intended public repository model:

AI-assisted, versioned research repository
for the MST–CRT–IET architecture stack

It should be interpreted as:

repository-architecture audit
AUDIT-ONLY
no theorem-status change

It should not be interpreted as:

theorem validation
proof correctness
external peer review
full synthesis claim

Future AI agents should read it before proposing branch merge, public release, or MST language work.

Repository navigation layer

The repository navigation map is:

docs/REPOSITORY_MAP.md

The documentation index is:

docs/README.md

Future AI agents should use these files as navigation anchors.

Navigation principle:

README.md = public entry
docs/REPOSITORY_MAP.md = full repository map
docs/README.md = documentation index
AGENTS.md = AI-agent entry rules
docs/AI_AGENT_CONTEXT.md = AI-agent memory

When adding or moving public-facing files, update:

README.md
docs/REPOSITORY_MAP.md
docs/READING_GUIDE.md
relevant directory README.md
docs/AI_AGENT_CONTEXT.md when architecture meaning changes

Directory README files should link back to:

repository root
repository map
reading guide
status labels
claims ledger

Do not add links that imply theorem-status promotion.

Do not use legacy technical indexes as the public entry path.

Public release model and Zenodo artifact registry

The public release model is:

docs/PUBLIC_RELEASE_MODEL.md

Public artifacts are registered under:

artifacts/
artifacts/zenodo/

Current registered Zenodo records:

artifacts/zenodo/19884063/
artifacts/zenodo/19937666/

Interpretation rule:

Zenodo records are staged public research summaries.
They are public checkpoints and citation anchors.
They are not peer review, institutional endorsement, or final theorem completion.

Do not copy PDFs into the repository unless explicitly instructed.

Do not import private source files associated with a Zenodo record unless explicitly approved.

Do not treat a Zenodo record as a claim-status upgrade.

Current record meanings:

19884063 = CRT synthesis / Degrees of Freedom / structural-collapse package
19937666 = MST determinization / closure / comparability / joint-admissibility package

## Public release interpretation rule
All future public releases follow this model:
```text
private R&D workspace
  -> human-approved release candidate
  -> status-labeled public artifact
  -> citation / non-claim boundary
  -> public registry entry
  -> optional source or proof mirror only if explicitly approved
```

Permanent interpretation rule:

Public repo = release and interpretation layer.
Private repos = R&D, memory, and raw work layer.
Zenodo = staged public research summary / citation anchor.

Future agents must not treat public release artifacts as:

peer-reviewed publication
institutional endorsement
final theorem completion
full private archive disclosure

Every public release must state:

what it is
what layer it belongs to
what status it has
how to cite it
what it does not claim
what remains private or unresolved

Default release behavior:

register first
link first
copy later only if explicitly approved

Do not import private source automatically.

Do not copy PDFs automatically.

Do not modify theorem or proof content during release registration.

This rule applies to all future staged releases, including Zenodo records, GitHub releases, proof artifacts, methodology artifacts, application artifacts, and architecture artifacts.

## Founding principles, emergence, and project provenance

The public-safe founding-principles record is:

```text
docs/FOUNDING_PRINCIPLES.md
```

The public-safe emergent-process interpretation is:

```text
docs/EMERGENT_RESEARCH_PROCESS.md
```

The public-safe provenance account is:

```text
docs/PROJECT_PROVENANCE.md
```

These files record the process interpretation that CRT developed through:

```text
practical market-structure problem
-> objective description constraints
-> admissibility and determinization
-> adoption and stability
-> robustness / escape / synthesis
```

This is the problem-forced abstraction path:

```text
UMOS / Genesis
  -> Exodus
  -> MST
  -> IET
  -> CRT
```

Future AI agents must preserve the following boundaries:

```text
Founding principles are methodology / governance principles, not theorem axioms by themselves.
Emergent process is a retrospective methodology interpretation, not proof of CRT correctness.
Project provenance is process history, not theorem validation.
GitHub history is provenance, not theorem validation.
AI assistance is not autonomous authorship or peer review.
Private raw provenance records should not be reproduced in public docs.
```

Do not claim that AI independently discovered or validated CRT.

Do not claim that the emergent-process interpretation proves any theorem.

Do not publish raw internal reports as public methodology documents.

Do not reproduce private repository URLs or private raw text.

## Public argument layer

The current public argument layer is:

```text
docs/PUBLIC_ARGUMENT_MAP_v0_1.md
mst/arguments/MST_PUBLIC_ARGUMENT_v0_1.md
crt/arguments/CRT_PUBLIC_ARGUMENT_v0_1.md
iet/arguments/IET_PUBLIC_ARGUMENT_v0_1.md
```

These files provide a public-readable, status-labeled path through the MST–CRT–IET stack.

They should be interpreted as:

```text
argument / interpretation artifacts
```

They should not be interpreted as:

```text
proof artifacts
theorem statements
peer-reviewed publications
full synthesis claims
private source mirrors
```

Future AI agents must preserve these boundaries.

Do not import private source into public argument modules unless explicitly instructed.

Do not promote argument modules into theorem files.

Do not remove their non-claim boundaries.

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

Legacy technical archive reclassification

Legacy CRT technical archive material is preserved for provenance and research traceability.

Examples include:

THEORY_INDEX.md
PUBLICATION_STATUS.md
STATUS_GLOSSARY.md
papers/foundations/
papers/open-systems/
proofs/supplement/
older scaffold files under papers/

These files should not be treated as the current top-level public architecture.

Current interpretation rule:

README.md                    = public entry
docs/ARCHITECTURE.md         = current architecture reference
docs/STATUS_LABELS.md        = canonical status-label reference
docs/CLAIMS_LEDGER.md        = current claim-status board
docs/LEGACY_ARCHIVE.md       = how to read legacy technical material
THEORY_INDEX.md              = deep technical archive index
PUBLICATION_STATUS.md        = publication / preprint / archival status ledger
STATUS_GLOSSARY.md           = legacy archive terminology

Do not use THEORY_INDEX.md as the public entry page.

Do not infer current theorem status directly from old archive language.

Do not treat publication status as theorem status.

Do not treat archived or DOI-linked material as peer-reviewed unless explicitly stated.

Architecture deep scan

The current public architecture scan is:

docs/ARCHITECTURE_DEEP_SCAN_v0_1.md

This file records the state after:

public research surface rebuild
AI-agent memo
status-label unification
IET naming resolution
proof-status sidecar ledgers
legacy technical archive reclassification

Future agents must read it before proposing:

MST_LANGUAGE_v0_1
MST_STRATIFIED_CORE_v0_1
CRT synthesis restructuring
IET expansion
legacy archive migration

The scan’s main verdict is:

the next architecture task is MST language first, then stratified MST core

Do not skip directly to stratified core before defining the language boundary.

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

Proof status sidecar ledgers

The current public rebuild phase uses sidecar ledgers for proof artifact status.

Canonical proof-status ledgers:

proofs/STATUS.md
proofs/supplement/STATUS.md

These ledgers record status metadata without modifying theorem or proof content.

Future agents must read these ledgers before interpreting proof supplement files.

The current supplement status boundaries are:

main.tex                 = ARCHIVAL / CONDITIONAL technical supplement
appendix_a_bridge.tex    = CONDITIONAL / CLOSED within stated bridge scope
appendix_b_el.tex        = CLOSED within stated execution-layer scope
appendix_c_iet.tex       = SKETCH / CONDITIONAL

Do not cite appendix_c_iet.tex as a final full IET proof.

Do not treat the proof supplement as external peer review.

Do not treat the proof supplement as unconditional full synthesis.

Proof publication policy

The proof publication policy is:

docs/PROOF_PUBLICATION_POLICY.md

The proof artifact status template is:

proofs/ARTIFACT_STATUS_TEMPLATE.md

The proof taxonomy is:

proofs/closed/
proofs/conditional/
proofs/sketches/
proofs/audits/
proofs/superseded/
proofs/supplement/

Future AI agents must not treat public proof artifacts as global theorem completion.

A proof artifact may be public while remaining:

CLOSED
CONDITIONAL
SKETCH
AUDIT-ONLY
SUPERSEDED
OPEN
WORKING

Do not move proof artifacts between taxonomy directories unless:

1. status metadata is updated,
2. citation boundary is updated,
3. docs/AI_AGENT_CONTEXT.md is updated,
4. the change is explicitly approved by the human maintainer.

Key public-misreading boundaries:

MST v2.16.4 does not imply full property (4) or AC-6.
IET v2.3 is process-specific and conditional.
FDT-related artifacts are audit / conditional unless external dependencies are discharged.
The full MST–CRT–IET synthesis is not unconditional.

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

## IET naming resolution
Canonical repository convention:
```text
IET = Inferential Equilibrium Theory
```

Legacy scaffold files may have used IET to mean institutional / interpretive / invariant escape material.

Those legacy uses should now be interpreted as application-layer material unless explicitly formalized as Inferential Equilibrium Theory.

Do not treat papers/iet/ legacy scaffold files as canonical definitions of IET.

Canonical IET references are:

* docs/IET_NAMING.md
* iet/README.md
* docs/ARCHITECTURE.md
* docs/TERMINOLOGY.md
* papers/foundations/IET_STATUS.md

## Current priority order

The current repo priority is:

1. Rebuild public research surface. DONE and merged into `main`.
2. Add AI-agent context memo. DONE and merged into `main`.
3. Unify status vocabulary. DONE and merged into `main`.
4. Resolve IET naming conflict. DONE and merged into `main`.
5. Add proof artifact status ledgers. DONE and merged into `main`.
6. Reclassify legacy technical archive / `THEORY_INDEX.md`. DONE and merged into `main`.
7. Add architecture deep-scan artifact. DONE and merged into `main`.
8. Add proof publication policy and taxonomy. DONE and merged into `main`.
9. Add independent project and privacy boundary. DONE and merged into `main`.
10. Add execution, role, and adversarial audit protocols. DONE and merged into `main`.
11. Add methodology retrospective. DONE and merged into `main`.
12. Add methodology case study and development timeline. DONE and merged into `main`.
13. Add branch-level rebuild audit. DONE and merged into `main`.
14. Add repository navigation layer. DONE by current navigation pass.
15. Add public release model and Zenodo artifact registry. DONE by current artifact-registry pass.
16. Add founding principles, emergent process, and project provenance. DONE by current provenance pass.
17. Add public argument layer v0.1. DONE by current argument-layer pass.
18. Design `MST_LANGUAGE_v0_1`. NEXT.
19. Then design `MST_STRATIFIED_CORE_v0_1`.

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
