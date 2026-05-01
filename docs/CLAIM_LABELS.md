Claim Labels

Purpose

This document explains how claim-level labels relate to the repository-wide status-label system.

The canonical status-label system is defined in:

* docs/STATUS_LABELS.md

This file is a claim-facing companion, not an independent status system.

Claim-level labels

CONJECTURE

A proposed statement with no proof.

Canonical status mapping:

* usually OPEN or WORKING

⸻

SKETCH

A partially developed argument or proof outline.

Canonical status mapping:

* SKETCH

⸻

PARTIAL

A result that holds under limited scope.

Canonical status mapping:

* usually CONDITIONAL

⸻

CONDITIONAL

A result that depends on explicit assumptions.

Canonical status mapping:

* CONDITIONAL

⸻

PROVED

A claim with a proof within stated assumptions and scope.

Canonical status mapping:

* CLOSED if internally audited and version-locked
* CONDITIONAL if assumptions remain active
* not automatically peer-reviewed

Important:

PROVED must not be used to imply global synthesis, external peer review, or discharge of unstated assumptions.

⸻

AUDIT-LOCAL

A result or finding verified only in an internal or limited audit context.

Canonical status mapping:

* usually AUDIT-ONLY
* sometimes CLOSED within limited scope

⸻

DEPRECATED

A result no longer considered current.

Canonical status mapping:

* usually SUPERSEDED

Rules

* Labels must not be omitted from major artifacts.
* Labels must not be upgraded without justification.
* Claim labels must be interpreted through docs/STATUS_LABELS.md.
* Peer review must be stated separately from claim status.
* AI-assisted audit must not be described as peer review.

Forbidden

* Implicit promotion
* Silent relabeling
* Treating CLOSED as peer-reviewed
* Treating SEALED as peer-reviewed
* Treating ARCHIVAL as peer-reviewed
* Treating CONDITIONAL as unconditional
* Treating SKETCH as a complete proof
* Treating AUDIT-ONLY as a theorem

⸻
