# Public Release Model
## Purpose
This document defines how staged research artifacts move from private R&D into the public CRT research repository.
## Core model
The repository follows a software-engineering-style release model for theory development.
```text
private R&D workspace
  -> curated release candidate
  -> staged public research summary
  -> archival citation anchor
  -> public registry and interpretation layer
```

Private R&D workspace

Private repositories and private working materials are used for:

* raw theory development
* failed proof paths
* internal audits
* exploratory notes
* private memory
* unfinished theorem drafts
* non-public discussions
* mixed-language material

Private R&D material does not enter the public repository automatically.

Zenodo records

Zenodo records in this project are staged public research summaries.

They freeze a citable state of the research program at a given time.

They do not constitute:

* formal peer review
* institutional endorsement
* final theorem completion
* full private archive disclosure
* validation of the entire MST–CRT–IET synthesis

Public GitHub repository

This public GitHub repository is the release registry and interpretation layer.

It records:

* what was released
* where it was released
* what layer it belongs to
* how it should be cited
* what status label applies
* what it does not claim
* which dependencies or limitations remain open

## Permanent interpretation rule
```text
Public repo = release and interpretation layer.
Private repos = R&D, memory, and raw work layer.
Zenodo = staged public research summary / citation anchor.
```

Every public release must state what it is, what layer it belongs to, what status it has, how to cite it, what it does not claim, and what remains private or unresolved.

Private public-candidate gate

Before theory content is released publicly, it should pass through a private public-candidate area.

Required flow:

private R&D workspace
  -> private public-candidate area
  -> audit / review / demotion
  -> human approval
  -> public release registry / public summary / public artifact

The public-candidate area is still private.

It exists to prepare public-safe artifacts before public release.

See:

* docs/PUBLIC_CANDIDATE_GATE.md

Release artifact rule

A public release artifact should include:

Status:
Peer review:
Review status:
AI assistance:
Citation status:
Scope:
Dependencies:
Known limitations:
Do not cite as:
Related repository paths:

Import rule

A public release record may be registered without copying the full artifact into GitHub.

Default policy:

link first
copy later only if explicitly approved

Source mirror rule

Source files from private repositories should not be mirrored unless they pass:

* English-only review
* private-material review
* status-label review
* peer-review disclosure check
* AI-assistance disclosure check
* theorem-promotion check
* human approval

Proof extraction rule

Proof artifacts should not be extracted from a release into proofs/ unless:

* the target proof-status directory is explicit
* artifact status metadata is added
* citation boundary is stated
* assumptions are listed
* known limitations are recorded
* human approval is given

Default interpretation

A staged research summary should be interpreted as:

public checkpoint
citable archival state
research summary
status-labeled release artifact

It should not be interpreted as:

final monograph
peer-reviewed publication
institutional validation
complete proof archive
unconditional synthesis theorem

⸻
