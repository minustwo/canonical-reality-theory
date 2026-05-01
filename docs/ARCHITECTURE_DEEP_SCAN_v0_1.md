# Architecture Deep Scan v0.1
## Status
Status: ARCHITECTURE / AUDIT-ONLY.
Peer review: Not externally peer reviewed.
AI assistance: This scan is AI-assisted and human-directed.
Claim-status impact: No theorem-status change.
Scope: Public repository architecture only.
## Purpose
This document records the current public architecture state of the CRT research repository after the public-research rebuild.
It is a repo-level architecture scan.
It is not:
- a theorem statement
- a proof
- a synthesis claim
- a peer-reviewed publication
- a replacement for technical artifacts
## Executive verdict
The repository is now best understood as:
```text
an AI-assisted, versioned research repository
for the MST–CRT–IET architecture stack

It is no longer treated as:

* a paper repository
* a software package
* a finished theorem archive
* a raw draft dump

The main remaining work is architectural hardening:

status-stable public surface
+ legacy technical archive
+ explicit dependency map
+ future stratified core

Current repository layers

1. Public research surface

Primary files:

* README.md
* docs/ARCHITECTURE.md
* docs/STATUS.md
* docs/STATUS_LABELS.md
* docs/CLAIMS_LEDGER.md
* docs/OPEN_PROBLEMS.md
* docs/READING_GUIDE.md
* docs/RESEARCH_PROCESS.md
* docs/TERMINOLOGY.md

Role:

current public entry and governance layer

2. AI-agent memory layer

Primary files:

* AGENTS.md
* docs/AI_AGENT_CONTEXT.md

Role:

operational memory for future AI-assisted repo work

3. Legacy technical archive layer

Primary files and directories:

* THEORY_INDEX.md
* PUBLICATION_STATUS.md
* STATUS_GLOSSARY.md
* papers/foundations/
* papers/open-systems/
* proofs/supplement/
* older scaffold files under papers/

Role:

deep technical archive and historical CRT map

This layer is preserved for provenance and research traceability.

It should be interpreted through:

* docs/LEGACY_ARCHIVE.md
* docs/STATUS_LABELS.md
* docs/CLAIMS_LEDGER.md
* proofs/STATUS.md
* proofs/supplement/STATUS.md

MST scan

Current public forms

MST has two public-facing forms.

1. Archival / legacy foundation form

Legacy MST material should be treated as:

ARCHIVAL Layer-1 core
pre-stratified
not final stratified MST core

Known boundary:

(4') established
full property (4) not automatic
no automatic AC-6 promotion

2. Decomposed public presentation

The papers/mst/ material is a decomposed determinization presentation.

It is useful for public explanation and entry-level framing.

It should not be confused with the full historical MST core.

MST architecture gap

The main MST gap is not another paper section.

The main MST gap is:

MST language formalization
+ MST stratified core

Future work should separate:

* Layer-1 admissibility
* Layer-2 justification
* CRT break / escape interfaces
* IET dynamic dependencies

CRT scan

CRT is the bridge, escape-cost, robustness, and synthesis layer.

CRT includes:

* bridge hierarchy
* correctness / robustness alignment
* source-layer escape
* C_min
* break paths
* traceability
* synthesis dependencies

Current boundary:

* CRT is not MST.
* C_min should not be folded back into MST Layer 1.
* Bridge claims remain conditional unless assumptions are explicit.
* Full synthesis is not claimed unconditionally.

IET scan

Canonical repository convention:

IET = Inferential Equilibrium Theory

IET is the dynamic adoption and stochastic-selection layer.

Current boundary:

IET v2.3 is conditional and process-specific.
Claims involving unique P^{canon} depend on explicit MST property (4) / MST-4 assumptions.
Reduced sliding-window results do not imply full dynamic canonicality.

Legacy institutional / interpretive uses of IET are now treated as application-layer material unless explicitly formalized as Inferential Equilibrium Theory.

Applications scan

Applications include:

* institutional systems
* governance systems
* market systems
* DeFi systems
* AI systems
* organizational systems

Applications may illustrate, diagnose, or instantiate theory.

They do not automatically prove MST, CRT, IET, or full synthesis claims.

Application material belongs under:

applications/

unless explicitly promoted through reviewed formalization.

Proof artifact scan

Proof artifacts may be public, but public proof artifacts do not imply global theorem completion.

Current proof-status references:

* proofs/STATUS.md
* proofs/supplement/STATUS.md

Current supplement boundary:

main.tex                 = ARCHIVAL / CONDITIONAL technical supplement
appendix_a_bridge.tex    = CONDITIONAL / CLOSED within stated bridge scope
appendix_b_el.tex        = CLOSED within stated execution-layer scope
appendix_c_iet.tex       = SKETCH / CONDITIONAL

No proof supplement should be read as:

* external peer review
* unconditional synthesis
* full dynamic canonicality
* proof of all MST assumptions

Status-system scan

The canonical status system is:

* docs/STATUS_LABELS.md

Canonical labels:

ARCHIVAL
SEALED
CLOSED
CONDITIONAL
SKETCH
AUDIT-ONLY
OPEN
SUPERSEDED
WORKING

Older local labels should be interpreted through this system.

Important non-equivalences:

SEALED ≠ peer reviewed
CLOSED ≠ peer reviewed
ARCHIVAL ≠ peer reviewed
PROVED ≠ globally complete
AUDIT-ONLY ≠ theorem
Zenodo DOI ≠ peer review
AI-assisted audit ≠ peer review

Architecture gaps

The current public repository is structurally sound but still has architecture gaps.

Gap 1 — MST language not formalized

The repo needs a typed public MST language covering:

* admissibility
* justification
* break / escape
* dynamics dependencies
* application boundary

Recommended future artifact:

MST_LANGUAGE_v0_1

Gap 2 — MST core is pre-stratified

MST v2.16.4 should remain archival.

The next MST core should be stratified rather than monolithic.

Recommended future artifact:

MST_STRATIFIED_CORE_v0_1

Gap 3 — Layer-2 not integrated

Layer-2 justification material shows that Layer-1 admissibility / uniqueness is insufficient for final canonicality.

Future architecture should explicitly separate:

canonical_L1
canonical_L2
canonical_CRT
canonical_IET

Gap 4 — CRT escape belongs to a separate layer

C_min, break paths, and source-layer escape should remain CRT-layer objects.

They should not be forced into MST Layer 1.

Gap 5 — IET remains conditional

IET should remain conditional on explicit MST and process assumptions.

Do not treat IET as full dynamic canonicality.

Gap 6 — legacy archive still needs gradual migration

Legacy material is preserved and now reclassified.

Future migration should be gradual and status-driven.

Recommended next architecture files

Only after this scan is accepted, the next architecture files should be:

MST_LANGUAGE_v0_1
MST_STRATIFIED_CORE_v0_1

Suggested order:

1. MST_LANGUAGE_v0_1
2. MST_STRATIFIED_CORE_v0_1

Reason:

language before core

Do not design the stratified core before the typed language boundary is explicit.

Non-actions

Do not do the following at this stage:

* do not write synthesis paper
* do not expand MST paper
* do not restart Sig0 / FDT proof passes
* do not start IET L6 / L7
* do not claim Equivalence III proof completion
* do not fold CRT escape into MST Layer 1
* do not treat applications as proof
* do not import private raw material

Final verdict

The public repository has reached a stable research-repository architecture.

The next theoretical architecture task is not more documentation.

It is:

define the public MST language
then define the stratified MST core

This document records the architecture state before that transition.

⸻
