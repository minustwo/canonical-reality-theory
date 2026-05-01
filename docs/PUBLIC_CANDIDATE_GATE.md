# Public Candidate Gate
## Purpose
This document defines the private-to-public release gate for theory content.
The public repository is a release and interpretation layer.
It is not the private R&D workspace.
Theory content should not move directly from private R&D into the public repository.
## Release path
The required release path is:
```text
private R&D workspace
  -> private public-candidate area
  -> audit / review / demotion
  -> human approval
  -> public release registry / public summary / public artifact
```

Private public-candidate area

Each private research repository may contain a public-candidates/ directory.

This area is still private.

It is used to prepare public-safe release candidates before anything enters the public repository.

A public candidate should be:

* English only
* status-labeled
* free of private raw notes
* free of raw chat logs
* free of unnecessary personal identifiers
* free of private repository URLs
* explicit about peer-review status
* explicit about AI assistance
* explicit about citation boundaries
* explicit about non-claims
* checked for theorem promotion

Candidate lifecycle

A candidate may move through:

WORKING
  -> PUBLIC-CANDIDATE
  -> AUDITED
  -> APPROVED-FOR-PUBLIC
  -> RELEASED

A candidate may also be marked:

REJECTED
SUPERSEDED
PRIVATE-ONLY

Required candidate files

A public-candidate package should include:

README.md
STATUS.md
AUDIT.md
RELEASE_CHECKLIST.md

For larger artifacts, additional files may be added.

Public release rule

The public repository should receive only the approved public-facing artifact, summary, registry entry, or release note.

The public repository should not receive:

* raw private notes
* failed attempts
* private audit conversations
* unfinished proof drafts
* private memory files
* unapproved source mirrors
* unapproved PDFs

Default rule

Register first.

Link first.

Copy later only if explicitly approved.

⸻
