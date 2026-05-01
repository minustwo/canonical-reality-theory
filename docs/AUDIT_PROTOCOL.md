Audit Protocol

Purpose

This document defines the public audit protocol for future technical additions.

Audit goals

An audit should determine whether a document is:

* Internally consistent
* Correctly scoped
* Properly labeled
* Public-safe
* Free of theorem promotion
* Free of private-source leakage

Audit levels

Level 0 — Structural audit

Checks file organization, naming, English-only status, and repository fit.

Level 1 — Claim audit

Checks whether claims match their stated status.

Questions:

* Is a conditional result labeled conditional?
* Is a sketched proof labeled sketched?
* Is a conjecture labeled conjectural?
* Are bridge assumptions explicit?

Level 2 — Dependency audit

Checks whether definitions, lemmas, propositions, and bridge claims depend on unstated assumptions.

Level 3 — Public release audit

Checks whether the file is suitable for public release.

Questions:

* Does it contain private notes?
* Does it contain unpublished sensitive material?
* Does it expose raw internal audit language?
* Does it include non-English material?
* Has the human maintainer approved release?

Audit output

Audit output should clearly state:

* Verdict
* Scope
* Files checked
* Blocking issues
* Non-blocking issues
* Required changes before release

No silent correction

Auditors should not silently rewrite theorem content. Structural or editorial changes should be separated from mathematical changes.

Audit modes

This repository uses three audit modes.

1. Iterative adversarial audit

A context-preserving audit loop where one agent proposes and another challenges the structure.

Purpose:

* expose hidden assumptions
* locate overclaims
* identify missing dependencies
* support status demotion

2. Adversarial generation

An agent attempts alternative constructions, counterexamples, or independent formulations.

Purpose:

* break path dependency
* test robustness of assumptions
* uncover boundary cases

3. Context-reset audit

A context-reset audit is performed in a new session or isolated context.

The artifact is presented as standalone.

The auditor should not rely on prior discussion history.

Purpose:

* simulate first-contact external-reader behavior
* reveal hidden assumptions inherited by prior sessions
* test whether the artifact is interpretable without private context

Context-reset audit requirements

A context-reset audit should be used:

* before claiming closure
* before promoting a claim to stronger status
* when hidden dependencies are suspected
* when an artifact survives multiple internal audit rounds
* when a public artifact must be readable without private context

At least one context-reset audit is recommended before any CLOSED or SEALED status assignment.

This recommendation does not imply peer review.

Context-reset prompt discipline

A context-reset audit prompt should not ask the auditor to prove the claim.

Recommended framing:

You are an external auditor.
You are given a standalone research artifact.
You have no access to prior discussions.
Task:
- identify hidden assumptions
- test whether the claim is unconditional or conditional
- attempt counterexample construction
- identify missing definitions or dependencies
- do not repair the proof unless asked
- do not assume the claim is correct

Audit output categories

Audit results should be classified as:

ACCEPT-WITHIN-SCOPE
ACCEPT-WITH-MINOR-FIXES
NEEDS-STRONGER-ASSUMPTIONS
COUNTEREXAMPLE-FOUND
OPEN-DEPENDENCY
UNDECIDABLE-WITHOUT-EXTERNAL-INPUT
SUPERSEDED-BY-CORRECTION

Peer-review boundary

Internal audit, adversarial audit, context-reset audit, and AI-assisted review are not formal peer review.

They are repository methods for status discipline.
