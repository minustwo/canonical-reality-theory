# Status Labels
## Purpose
This document defines the canonical status labels for the public CRT research repository.
These labels govern:
- definitions
- theorem statements
- proof artifacts
- audit records
- open problems
- release notes
- architecture documents
- archived materials
A public artifact must be interpreted together with its status label.
Publication, archival upload, DOI assignment, internal audit, and AI-assisted review do not by themselves change status.
---
## Canonical labels
### ARCHIVAL
A publicly archived or version-tagged research artifact.
Typical use:
- Zenodo record
- release-tagged manuscript
- frozen public version
- historical public anchor
Important:
ARCHIVAL does not mean peer-reviewed.
ARCHIVAL does not mean theorem-complete.
ARCHIVAL does not imply that all dependencies are discharged.
---
### SEALED
An interface, theorem statement, definition, or artifact frozen within this research program.
Typical use:
- frozen theorem statement
- frozen interface
- frozen dependency boundary
- version-locked technical report
Important:
SEALED does not mean peer-reviewed.
SEALED means the artifact should not be silently modified.
---
### CLOSED
An artifact internally audited and version-locked within stated scope.
Typical use:
- internally reviewed proof artifact
- closed audit line
- scope-complete technical note
- version-locked internal result
Important:
CLOSED does not mean peer-reviewed.
CLOSED means no major revision is expected within the stated scope.
---
### CONDITIONAL
A claim, theorem, bridge, or result that holds only under explicit assumptions.
Typical use:
- bridge theorem with stated conditions
- synthesis claim dependent on MST / IET assumptions
- process-specific dynamic result
- domain result requiring explicit model assumptions
Important:
A CONDITIONAL result must be cited with its assumptions.
Do not cite CONDITIONAL artifacts as unconditional.
---
### SKETCH
A coherent proof outline, argument sketch, or structural derivation that is not a complete proof.
Typical use:
- proof sketch
- exploratory derivation
- outline of a possible theorem route
- informal structural argument
Important:
SKETCH is not a completed proof.
Do not cite SKETCH artifacts as theorem-level results.
---
### AUDIT-ONLY
An artifact that records audit, counterexample, dependency analysis, independence analysis, or review findings.
Typical use:
- counterexample record
- independence audit
- dependency check
- adversarial review note
- proof-status diagnostic
Important:
AUDIT-ONLY artifacts are not theorem statements.
They may affect theorem status, but they are not themselves promoted results.
---
### OPEN
A formally recognized open problem, unresolved dependency, or incomplete research direction.
Typical use:
- open problem
- unresolved theorem dependency
- incomplete bridge condition
- future formalization task
Important:
OPEN means no closure is claimed.
---
### SUPERSEDED
A historical artifact that has been replaced by a newer version or corrected statement.
Typical use:
- old theorem version
- replaced proof draft
- corrected technical report
- pre-erratum artifact
Important:
SUPERSEDED artifacts should not be cited as current.
They may be retained for provenance.
---
### WORKING
An active draft, unstable artifact, or ongoing research file.
Typical use:
- active note
- draft specification
- evolving formalization
- pre-release architecture file
Important:
WORKING material may change substantially.
Do not cite WORKING artifacts as stable.
---
## Non-status terms
The following terms may appear in older files but should be interpreted through the canonical labels above.
| Legacy / local term | Canonical interpretation |
|---|---|
| `PROVED` | Usually `CLOSED` or `CONDITIONAL`, depending on scope and assumptions |
| `REVIEWED` | Internal review only unless explicitly peer-reviewed |
| `PUBLIC-SAFE` | Release-boundary label, not a mathematical status |
| `PRIVATE-ONLY` | Access-boundary label, not a mathematical status |
| `DEPRECATED` | Prefer `SUPERSEDED` unless invalidity is specifically meant |
| `DRAFT` | Usually `WORKING` |
| `SKETCHED` | `SKETCH` |
| `AUDIT-LOCAL` | Usually `AUDIT-ONLY` or `CLOSED` within limited scope |
| `ACCEPTED diagnostic` | `AUDIT-ONLY` or `CLOSED` diagnostic artifact, depending on scope |
| `Candidate theorem` | Usually `OPEN`, `WORKING`, or `CONDITIONAL` |
---
## Peer-review boundary
None of the canonical labels imply external peer review.
In particular:
- ARCHIVAL is not peer review.
- SEALED is not peer review.
- CLOSED is not peer review.
- INTERNAL REVIEW is not peer review.
- AI-assisted audit is not peer review.
- Zenodo DOI assignment is not peer review.
- GitHub publication is not peer review.
- arXiv or SSRN availability is not peer review.
Only explicit acceptance by a recognized peer-reviewed venue should be described as peer review.
---
## Artifact header schema
Major artifacts should include, where applicable:
```text
Status:
Peer review:
Review status:
AI assistance:
Citation status:
Scope:
Dependencies:
Known limitations:
```

⸻

Citation discipline

Cite artifacts with their status.

Do not cite:

* CONDITIONAL artifacts as unconditional
* SKETCH artifacts as complete proofs
* AUDIT-ONLY artifacts as theorem statements
* SUPERSEDED artifacts as current
* ARCHIVAL artifacts as peer-reviewed unless explicitly peer-reviewed

⸻

Default rule

If unsure, use the weaker status label.

Do not silently promote status.

⸻
