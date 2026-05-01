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
