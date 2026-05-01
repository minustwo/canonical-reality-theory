# Status Glossary

> Canonical status labels are now defined in `docs/STATUS_LABELS.md`.
>
> This file preserves legacy CRT archive terminology and maps it to the canonical repository status system.
>
> If there is a conflict, use `docs/STATUS_LABELS.md` as the canonical reference.
>
> SEALED and CLOSED are internal archive workflow labels. They do not imply external peer review.

This glossary defines the status labels used in the CRT research archive.

---

## Archive status labels

### SEALED

A document version that is frozen and will not be modified. SEALED indicates
that an interface, theorem statement, or technical report has reached a stable
form used as a reference by downstream documents.

**SEALED does not mean peer-reviewed.** It is an internal archive workflow label.

*Example*: CRT Bridge Theorem Final v1.0.1 is SEALED. This means the theorem
statement is locked for citation purposes within this research program.

---

### CLOSED

A document that has passed internal adversarial review within the CRT research
program and is not expected to receive further major revisions.

**CLOSED does not mean peer-reviewed.** It reflects the internal review process,
not external journal or conference peer review.

SEALED and CLOSED are internal archive workflow labels.
They do not imply external peer review.

*Example*: CRT Bridge Hierarchy v0.3 is CLOSED. This means the hierarchy has
passed internal scrutiny and the terminology is stable.

---

### DRAFT

A working document under active development. Content may change substantially.

---

### ACCEPTED (diagnostic)

A diagnostic artifact (stress-test suite, audit report, cut suite) that has
passed internal review and is accepted as a diagnostic baseline.

**Diagnostic artifacts are not theorem papers.** They provide empirical or
structural support for theoretical claims, but do not constitute proofs.

*Example*: CRT Language Stress Test Suite v0.3 is an accepted diagnostic
artifact. It shows that 16 formal languages can be adapted to CRT, but it
is not itself a theorem.

---

## Publication status labels

### Peer-reviewed publication

A work accepted by a peer-reviewed journal or conference proceedings after
external review. **CRT currently has no peer-reviewed publications.**

---

### Preprint / technical report

A publicly available document that has not undergone external peer review.
Preprints may be submitted for peer review or distributed as technical reports.

*Example*: The synthesis paper "When Correctness, Robustness, and Stability
Coincide" is available as a preprint on Zenodo
([DOI 10.5281/zenodo.19871473](https://doi.org/10.5281/zenodo.19871473)).
It has not been peer-reviewed.

---

### Submitted / under review

A manuscript formally submitted to a venue for peer review.

---

### On hold (arXiv)

A manuscript submitted to arXiv that is pending moderation or awaiting
prerequisite conditions. "On hold" is not a rejection; it means the
submission is queued.

---

### Pending review (SSRN)

A manuscript uploaded to SSRN that has not yet been cleared for public
display. SSRN pending review is not peer review.

---

## Claim type labels

### Theorem

A formally proved result within the CRT framework. Requires a proof that
has passed internal adversarial review.

### Candidate theorem

A result that is conjectured and empirically supported, but not yet formally
proved within CRT's sealed axioms.

*Example*: The CJC avoidance conditions (normality + acyclicity, stratification,
priority ordering) are candidate theorems. They are verified in the CJC boundary
cut suite but not yet formally proved as a theorem within CRT.

### Conjecture

A proposed result for which there is theoretical motivation but no proof.

### Diagnostic result

A result from a stress-test, audit, or cut suite. Supports theoretical claims
but is not itself a proof.

*Example*: "All 16 tested languages produce no unexpected CRT adapter failures"
is a diagnostic result from the Language Stress Test Suite v0.3.

### Empirical / application observation

An observation about a real system that instantiates or motivates CRT concepts.

*Example*: CAPO/AgentHub $C_{\min}^{\mathrm{ctrl}} = 1$ is an application
observation from DeFi CRT Verification v0.4.

---

## Extension boundary labels

### CJC (Circular Justification Consistency)

A new classical justification boundary discovered in the CRT language stress tests.
Justification validity is globally circular (extension-dependent). Not a failure
of CRT core; a boundary of the NAA reformulation theorem's applicability.

### QNL (Quantum Non-Locality)

A quantum extension boundary. Classical/local CRT source-node model cannot
represent quantum entanglement. Extending CRT to quantum systems requires
new axioms (QNL-E1/E2/E3/E4).

---

*Status Glossary v0.1. 2026-04-29.*
*This glossary documents internal workflow labels and publication status categories.*
*It does not confer peer-review status on any document.*
