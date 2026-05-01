# Proof Artifact Status
## Purpose
This document defines how public proof artifacts in this repository should be read.
A proof artifact being public does not mean the full MST–CRT–IET synthesis is proved.
A proof artifact being archived does not mean it has undergone external peer review.
## Canonical status reference
Proof artifact status follows:
- `docs/STATUS_LABELS.md`
## Required interpretation
Every proof artifact should be read together with:
```text
Status:
Peer review:
Review status:
AI assistance:
Citation status:
Scope:
Dependencies:
Known limitations:

Proof artifact classes

Recommended classes:

proofs/closed/
proofs/conditional/
proofs/sketches/
proofs/audits/
proofs/superseded/
proofs/supplement/

Citation discipline

Do not cite:

* CONDITIONAL artifacts as unconditional
* SKETCH artifacts as complete proofs
* AUDIT-ONLY artifacts as theorem statements
* SUPERSEDED artifacts as current
* ARCHIVAL artifacts as peer-reviewed unless explicitly peer-reviewed

Peer-review boundary

The following are not peer review:

* internal audit
* AI-assisted review
* adversarial language-model review
* Zenodo archival upload
* DOI assignment
* GitHub publication
* arXiv or SSRN availability

Current proof-status ledgers

See:

* proofs/supplement/STATUS.md

⸻
