Role Model

Purpose

This document defines the role separation used in this AI-assisted research repository.

Role separation is required to avoid hidden claim promotion, self-review, and uncontrolled proof rewriting.

Core roles

Human maintainer

Final authority.

Responsibilities:

* accept or reject public releases
* decide what is public
* decide what is private
* approve theorem-status changes
* approve proof publication
* approve claim promotion or demotion
* preserve privacy and authorship boundaries

ChatGPT

Architecture and control layer.

Typical responsibilities:

* repository architecture
* status synthesis
* theory-boundary planning
* prompt generation
* workflow control
* cross-agent coordination

ChatGPT output is not peer review.

Claude

Default role: auditor.

Optional roles require explicit mode switching.

Allowed modes:

AUDITOR
PRODUCER
ADVERSARIAL PRODUCER

Default mode:

AUDITOR

Rules:

* Claude should not silently switch from auditor to producer.
* Producer and auditor roles must not be mixed implicitly.
* A producer output should not be accepted merely because the same model later approves it.
* Auditor mode should expose issues, hidden assumptions, overclaims, and counterexamples.
* Auditor mode should not silently repair proofs unless explicitly instructed.

Codex

Repository execution agent.

Responsibilities:

* create files
* update files
* apply bounded edits
* run checks
* commit and push
* report changed files and remote HEAD

Codex is not responsible for mathematical correctness.

Codex should not invent or improve theorem content.

Perplexity

Independent-style generator / cross-checker.

Typical role:

* alternative proof attempts
* external-style summaries
* independent formalization attempts
* search-informed cross-checking where appropriate

Perplexity output is not peer review.

Role-switch protocol

Any role switch must be explicit.

Examples:

Mode: PRODUCER
Task: draft a bounded artifact
Constraint: no theorem promotion
Mode: AUDITOR
Task: identify hidden assumptions
Constraint: do not repair, only expose
Mode: ADVERSARIAL PRODUCER
Task: attempt counterexample construction
Constraint: do not assume the claim is correct

Self-review boundary

Avoid:

producer -> same producer reviews itself -> acceptance

Preferred workflow:

producer -> independent auditor -> architecture synthesis -> human decision

Human acceptance

No AI system can independently:

* approve theorem status
* confer peer review
* certify proof correctness
* decide public release eligibility
* waive privacy boundaries
* publish private material

Default rule

If roles are unclear, treat the model as an auditor and do not permit theorem promotion.

⸻
