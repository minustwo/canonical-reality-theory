Adversarial Theory Development Protocol

Purpose

This document defines the adversarial reasoning workflow used in this repository.

The workflow is designed to discover hidden assumptions, prevent overclaiming, and preserve explicit theorem status.

It is not a substitute for external peer review.

Core idea

The repository uses a multi-agent adversarial workflow.

The goal is not to make every claim look stronger.

The goal is to identify the correct maturity status of each claim.

Typical status outcomes include:

CLOSED
CONDITIONAL
SKETCH
AUDIT-ONLY
OPEN
SUPERSEDED
WORKING

Standard loop

The standard loop is:

1. Proposal
2. Audit
3. Demotion or clarification
4. Re-audit
5. Human acceptance or rejection
6. Repository execution

Alternating adversarial audit

In alternating adversarial audit, one agent proposes a structure and another agent audits it.

Example:

Agent A proposes.
Agent B audits.
Agent A revises or demotes.
Agent B re-audits.
Human decides.

This helps expose hidden assumptions.

However, it remains an internal AI-assisted process.

It is not peer review.

Adversarial producer mode

An adversarial producer attempts to construct:

* counterexamples
* alternative formulations
* failure modes
* dependency violations
* boundary cases

Adversarial producer output should be treated as research input, not accepted proof.

Demotion discipline

When audit reveals hidden assumptions, the correct action is often demotion:

unconditional -> conditional
proved -> sketch
theorem -> candidate theorem
global -> process-specific
synthesis -> dependency map

Demotion is not failure.

Demotion is status correction.

Stopping rule

To avoid infinite refinement, an artifact may be considered stable within scope when:

* the claim is properly labeled
* assumptions are explicit
* dependencies are recorded
* no new structural blocker appears after adversarial review
* unresolved issues are moved to OPEN or CONDITIONAL
* the human maintainer accepts the status

Stable within scope does not mean peer-reviewed.

Stable within scope does not imply full synthesis.

Output categories

Audit outputs should be classified as:

ACCEPT-WITHIN-SCOPE
ACCEPT-WITH-MINOR-FIXES
NEEDS-STRONGER-ASSUMPTIONS
COUNTEREXAMPLE-FOUND
OPEN-DEPENDENCY
UNDECIDABLE-WITHOUT-EXTERNAL-INPUT
SUPERSEDED-BY-CORRECTION

Non-actions

Do not use adversarial review to silently:

* promote theorem status
* erase assumptions
* compress proofs
* merge layers
* declare peer review
* import private material

Default rule

The adversarial workflow is a method for status discipline.

It is not proof certification.

⸻
