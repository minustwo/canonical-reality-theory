# Canonical Reality Theory (CRT) Research Repository
This repository hosts the public research architecture for the **MST–CRT–IET** stack.
It is an **AI-assisted research repository** for versioned theory development.
It contains:
- architecture maps
- status ledgers
- proof-status records
- open problems
- release notes
- curated public technical artifacts
It is not:
- a finalized monograph
- a software package
- a peer-reviewed publication archive
- a raw private research dump
---
## Status
Active research repository.
Initial public architecture release.
Not a final proof of the full MST–CRT–IET synthesis.
Unless explicitly stated otherwise, materials in this repository have not undergone formal external peer review.
AI assistance, internal audit, adversarial review, Zenodo archival upload, DOI assignment, GitHub publication, arXiv availability, or SSRN availability do not constitute formal peer review.
---
## What this repo contains
- **MST** — structural canonicalization and admissibility layer
- **CRT** — bridge, escape-cost, robustness, and synthesis layer
- **IET** — inferential equilibrium / dynamic adoption / stochastic-selection layer
Institutional, governance, market, and AI-system applications are treated as application domains. They are not automatically proofs of MST, CRT, or IET claims.
---
## Current global verdict
| Layer | Artifact | Status | Boundary |
|---|---|---|---|
| MST | v2.16.4 | ARCHIVAL | Layer-1 core; establishes `(4')`, not automatic full `(4)` |
| CRT Bridge | Bridge hierarchy | CONDITIONAL / CLOSED by scope | Full bridge requires explicit bridge conditions |
| CRT Escape | `C_min` / Break interface | SEALED interface | Source-layer escape only unless extended |
| IET | v2.3 | CONDITIONAL | Reduced sliding-window / process-specific adoption theory |
| Synthesis | MST–CRT–IET stack | CONDITIONAL | Not claimed as an unconditional theorem |
| Sig0 / FDT | Closure artifacts | AUDIT / CONDITIONAL | Sandbox-internal closure with external dependencies |
---
## Status labels
Artifacts should be read with explicit maturity labels.
| Status | Meaning |
|---|---|
| `ARCHIVAL` | Publicly archived or version-tagged research artifact |
| `SEALED` | Interface, statement, or artifact frozen within this research program |
| `CLOSED` | Internally audited and version-locked within stated scope |
| `CONDITIONAL` | Holds only under explicit assumptions |
| `SKETCH` | Coherent outline, not a complete proof |
| `AUDIT-ONLY` | Audit, counterexample, or dependency record; not a theorem |
| `OPEN` | Open research problem |
| `SUPERSEDED` | Historical artifact; should not be cited as current |
| `WORKING` | Active draft or unstable research material |
---
## How to read this repository
Start with:
1. `docs/ARCHITECTURE.md`
2. `docs/STATUS.md`
3. `docs/CLAIMS_LEDGER.md`
4. `docs/OPEN_PROBLEMS.md`
5. `docs/READING_GUIDE.md`
For AI agents

Before proposing repository or theory changes, read:

* AGENTS.md
* docs/AI_AGENT_CONTEXT.md

Then explore:
- `mst/`
- `crt/`
- `iet/`
- `proofs/`
- `applications/`
- `releases/`
Legacy material may still exist under older paths during migration. Such material should be read through the status system, not as final theorem completion.
---
## What this release does not claim
This release does not claim:
- that MST property `(4)` is generally established
- that ICT determinization reaches AC-6 without additional assumptions
- that canonicality implies stochastic stability in full generality
- that the full MST–CRT–IET synthesis is proved unconditionally
- that AI-assisted audit is peer review
- that Zenodo archival upload is peer review
The current public architecture release records dependency structure and the conditional theorem landscape.
---
## Research process model
This repository uses software-style version control for theory development:
- theorem statements are versioned
- proof-status changes are recorded
- superseded drafts are preserved
- open questions are tracked like issues
- release notes distinguish mathematical changes from metadata changes
- audit artifacts are preserved as first-class research records
The objects under version control are not primarily code.
They are:
- definitions
- theorem statements
- proof artifacts
- assumptions
- counterexamples
- dependencies
- open problems
- release states
---
## Citation
Use artifact-specific citation information where available.
Zenodo DOI records provide public archival anchors, but they do not imply formal peer review.
See:
- `CITATION.cff`
- `docs/CLAIMS_LEDGER.md`
- `PUBLICATION_STATUS.md`
