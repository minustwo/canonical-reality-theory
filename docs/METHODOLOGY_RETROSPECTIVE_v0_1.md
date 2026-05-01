# Methodology Retrospective v0.1
## Status
Status: METHODOLOGY / AUDIT-ONLY.
Peer review: Not externally peer reviewed.
AI assistance: This retrospective describes an AI-assisted research workflow.
Claim-status impact: No theorem-status change.
Scope: Research-process reflection only.
## Purpose
This document records workflow lessons from the development of the CRT research stack.
It is not:
- a theorem statement
- a proof artifact
- a peer-reviewed methodology paper
- a claim that CRT is correct
- a claim that AI-assisted audit substitutes for peer review
- a productivity benchmark
- a guarantee of reproducibility
The purpose is to document a research process that may be useful for future work on this repository.
## Core framing
The repository is not only a collection of research artifacts.
It is also a versioned research process.
The process treats theory development as a controlled system involving:
- founding principles
- status labels
- audit loops
- open-question tracking
- release discipline
- error correction
- role separation
- AI-assisted execution
- human final authority
The working metaphor is:
```text
theory operating system

This metaphor does not mean the repository is software.

It means that research artifacts are versioned, audited, labeled, and released under explicit rules.

Principle 1 — Founding principles before theorem expansion

Before expanding a theory, the project should define its governing principles.

These principles constrain later claims, assumptions, definitions, and audit decisions.

A principle layer helps prevent uncontrolled theory growth.

Public rule:

Do not add theorem claims unless the governing principles and status boundary are clear.

Principle 2 — Status-first single source of truth

Every major artifact should have a status.

A repository without status labels becomes difficult to interpret.

Status labels help distinguish:

* closed artifacts
* conditional artifacts
* sketches
* audit notes
* superseded versions
* open problems
* working drafts

Public rule:

A public artifact must not be interpreted without its maturity label.

Principle 3 — Commit-level review loop

Large review cycles can be decomposed into smaller repository-level review cycles.

A typical loop is:

draft
audit
patch
status update
commit
review

This does not replace external peer review.

It is an internal discipline for reducing hidden assumptions before public release.

Principle 4 — Pre-audit patches

Before writing or releasing an artifact, foreseeable objections should be listed.

These are treated as pre-audit patches.

A pre-audit patch may address:

* missing assumptions
* edge cases
* notation ambiguity
* hidden dependency
* status overclaim
* broken citation boundary

Public rule:

Anticipated objections should be recorded before release when possible.

Principle 5 — Reviewer attack inventory

For important artifacts, the project may maintain an inventory of possible reviewer attacks.

An attack inventory records:

* likely objection
* severity
* affected claim
* existing response
* required patch
* remaining risk

This helps separate blocking issues from non-blocking issues.

Public rule:

A claim is not stable merely because it sounds coherent.
It must survive plausible attacks within its stated scope.

Principle 6 — Adversarial probe

The project should actively search for failure modes.

A failed generalization is useful when it identifies a boundary.

Adversarial probing may produce:

* counterexamples
* independence findings
* scope restrictions
* new boundary classes
* demotion from theorem to conditional result

Public rule:

A counterexample is a research artifact, not a failure to hide.

Principle 7 — Open-question ladder

Open questions should be decomposed into smaller rungs.

A question may move from:

OPEN
to PARTIAL
to CONDITIONAL
to CLOSED within scope

without becoming globally solved.

This allows progress without overclaiming.

Public rule:

Partially resolved is a valid research state.

Principle 8 — Path C freeze decisions

When two versions conflict and correctness cannot be resolved immediately, the safest action may be to freeze the inconsistency.

This avoids silently choosing a side.

A freeze records:

* conflicting versions
* known inconsistency
* current status
* deferred resolution path

Public rule:

When in doubt, freeze rather than force a theorem-status decision.

Principle 9 — Public error correction

Errors should be corrected without erasing provenance.

Where possible, the repository should avoid rewriting history to hide mistakes.

A correction should record:

* what was wrong
* what changed
* whether theorem status changed
* whether the previous artifact is superseded
* whether the correction is metadata-only or mathematical

Public rule:

Transparent correction is stronger than hidden revision.

Principle 10 — Cross-domain bridge discipline

Cross-domain synthesis should be treated carefully.

A bridge across domains does not automatically prove equivalence.

Bridge claims require:

* explicit assumptions
* directionality
* scope
* dependency tracking
* failure modes

Public rule:

Unification claims must remain conditional unless separately proved.

Principle 11 — AI role separation

AI systems may assist with:

* drafting
* refactoring
* adversarial audit
* counterexample search
* status synthesis
* repository execution
* cross-document consistency checks

AI systems must not be treated as:

* peer reviewers
* proof certifiers
* final authorities
* institutional endorsers

Public rule:

AI can assist the process.
The human maintainer decides public acceptance.

Principle 12 — Sustainable pacing

High-intensity research periods may produce useful artifacts, but sustained judgment requires pacing.

The human maintainer’s judgment is the final authority in this repository.

That judgment should not be degraded by uncontrolled sprint behavior.

Public rule:

Sustainable review discipline is part of research correctness.

Meta-invariant

The common invariant across these principles is honesty.

Honesty means:

* preserving status labels
* recording uncertainty
* admitting errors
* preserving audit trails
* demoting claims when needed
* separating proof from sketch
* separating audit from peer review
* separating public artifact from final theorem

The repository should prefer:

conditional and honest

over:

stronger but unsupported

Reusable workflow checklist

A future research line should begin by asking:

1. What are the governing principles?
2. What status label applies?
3. What assumptions are explicit?
4. What would a hostile reviewer attack?
5. What pre-audit patches are needed?
6. What open questions remain?
7. What artifacts are superseded?
8. What errors must be preserved?
9. What AI roles were used?
10. What does the human maintainer accept?
11. Does this require context-reset audit?
12. Does this change theorem status?

Relationship to other process documents

This retrospective should be read with:

* CODEX_WORKFLOW.md
* docs/FOUNDING_PRINCIPLES.md
* docs/EMERGENT_RESEARCH_PROCESS.md
* docs/ROLE_MODEL.md
* docs/AUDIT_PROTOCOL.md
* docs/ADVERSARIAL_THEORY_DEVELOPMENT_PROTOCOL.md
* docs/RESEARCH_PROCESS.md
* docs/STATUS_LABELS.md
* docs/PROOF_PUBLICATION_POLICY.md

The founding-principles and emergent-process documents are methodology artifacts. They do not validate theorem correctness or substitute for peer review.

Final note

This document records a methodology insight.

It does not validate any theorem by itself.

It does not substitute for external peer review.

It does not claim that the same workflow will reproduce the same research results elsewhere.

⸻
