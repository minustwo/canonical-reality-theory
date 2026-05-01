Research Process

Purpose

This repository uses software-style version control for theory development.

The objects under version control are research artifacts, not primarily code.

Versioned objects

The repository may version:

* definitions
* theorem statements
* proof drafts
* proof supplements
* audit records
* counterexamples
* status ledgers
* release notes
* open problems
* dependency maps

Release types

Release type	Meaning
metadata release	Updates DOI, README, citation, or status metadata
architecture release	Updates repository architecture or dependency map
theorem release	Adds or changes theorem/proof status
erratum release	Corrects a published or archived claim
audit release	Publishes audit artifacts without promoting theorem status
archival release	Freezes a version for citation or public record

## Independent project boundary
This repository is maintained as an independent personal research project.
The research process is human-directed and AI-assisted.
No repository process, audit pass, release tag, DOI assignment, or public upload should be interpreted as institutional endorsement or formal peer review unless explicitly stated.

## Execution and audit protocols
Repository execution and audit roles are governed by:
- `CODEX_WORKFLOW.md`
- `docs/ROLE_MODEL.md`
- `docs/ADVERSARIAL_THEORY_DEVELOPMENT_PROTOCOL.md`
- `docs/AUDIT_PROTOCOL.md`
The repository uses AI-assisted adversarial review and context-reset audits as internal methods for status discipline.
These methods do not constitute formal peer review.

Issue model

Research issues may track:

* definitions
* theorem dependencies
* open problems
* errata
* audit findings
* status changes
* metadata updates

Recommended issue labels:

type:definition
type:theorem
type:audit
type:open-question
type:erratum
type:metadata
status:open
status:conditional
status:blocked
status:sealed
status:superseded
layer:mst
layer:crt
layer:iet
layer:bridge
layer:escape
layer:dynamics
severity:blocking
severity:medium
severity:minor

Research issue template

A research issue should record:

Claim / Definition affected:
Current status:
Source artifact:
Problem:
Proposed resolution:
Does this change theorem status?

Rule

Repository maintenance must not silently promote theorem status.
