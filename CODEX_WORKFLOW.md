# Codex Workflow
## Purpose
This document defines how Codex should be used in this repository.
Codex is a repository execution agent.
Codex is not a theorem authority.
Codex is not a peer reviewer.
Codex is not responsible for mathematical correctness.
## Repository model
This repository is an AI-assisted, versioned research repository for the MST–CRT–IET architecture stack.
Codex may help execute:
- file creation
- file updates
- metadata maintenance
- status-ledger edits
- repository hygiene
- commit and push operations
- diff verification
Codex must not silently alter mathematical substance.
## Standard workflow
The default workflow is:
```text
1. Human + architecture agent decide what should be done.
2. Codex executes the repository change.
3. Codex reports diff, commit, push, and verification.
4. Human / architecture agent reviews the result.

Required prompt structure

Every Codex task should specify:

Goal:
Branch:
Context:
Hard constraints:
Files to create or update:
Exact content or bounded edits:
Verification:
Commit message:
Memo update requirement:

Hard rules

Codex must not:

* invent theorem statements
* rewrite proofs
* summarize proofs as if equivalent
* upgrade conditional claims
* remove status labels
* merge MST, CRT, and IET layers silently
* treat applications as proofs
* treat AI-assisted audit as peer review
* treat Zenodo DOI assignment as peer review
* import private raw material automatically
* modify proof artifacts unless explicitly instructed

Diff discipline

Before commit, Codex should run:

git diff --stat
git diff --name-only

For sensitive changes, Codex should also check that theorem/proof files were not modified:

git diff --name-only | grep -E "^(proofs/supplement/appendix_|proofs/supplement/main\.tex|papers/bridge/|papers/robustness/)" || true

Memo discipline

Every non-trivial repository architecture change must update:

docs/AI_AGENT_CONTEXT.md

If the change affects agent behavior, also update:

AGENTS.md

Future Codex prompts should include memo updates in the same commit unless explicitly waived.

Reporting requirement

After push, Codex should report:

current branch
remote HEAD SHA
changed files
confirmation that no theorem/proof files were modified
confirmation that docs/AI_AGENT_CONTEXT.md was updated when required

Default rule

If uncertain, Codex should preserve existing status labels and avoid claim promotion.

⸻
