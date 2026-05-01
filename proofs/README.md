Proof Artifacts

This directory contains or will contain public proof-related artifacts.

A proof artifact being public does not mean the full MST–CRT–IET synthesis is proved.
Public proof artifact does not mean global theorem completion.

Status metadata is maintained in sidecar ledgers before inline proof-file headers are added. Sidecar status ledgers do not modify theorem or proof content.

See:

docs/PROOF_PUBLICATION_POLICY.md
proofs/STATUS.md
proofs/supplement/STATUS.md
proofs/ARTIFACT_STATUS_TEMPLATE.md

Each proof artifact should carry status information:

Status:
Peer review:
Review status:
AI assistance:
Citation status:
Scope:
Dependencies:
Known limitations:

Recommended proof artifact classes:

proofs/closed/
proofs/conditional/
proofs/sketches/
proofs/audits/
proofs/superseded/
proofs/supplement/

Rule

Do not cite conditional, sketch, audit-only, or superseded artifacts as final theorem statements.
