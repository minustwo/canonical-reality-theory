# CRT Bridge Theory

This directory contains curated technical reports for the CRT Bridge theorem family.

**Publication status**: Technical-report / research-archive material.
These files are not peer-reviewed publications.

> "Sealed" and "Closed" are internal archive-status labels.
> They do not indicate external peer review.
> See [`STATUS_GLOSSARY.md`](../../STATUS_GLOSSARY.md) for definitions.

---

## Core result

**Bridge Sandwich** (Weak Bridge, SEALED v1.0.1):

$$\mathrm{TracedSCSet}_T(\Pi)
\;\subseteq_{\mathrm{C1+C2}}\;
\mathrm{UnbreakSet}_T(\Pi)
\;\subseteq_{\mathrm{C5_R}}\;
\mathrm{SCSet}_T(\Pi)$$

**Full Bridge** requires trace-completeness (C6):

$$\mathrm{SCSet}_T(\Pi) \subseteq \mathrm{CertReach}_T(\Pi)$$

Full Bridge conditions: C1 + C2 + C5_R + C6.
C3 and C4 are sufficient route to C5_R, not primitive Bridge conditions.

---

## Files

- **[`CRT_BRIDGE_THEOREM_FINAL_v1_0_1.md`](CRT_BRIDGE_THEOREM_FINAL_v1_0_1.md)** (SEALED) — Main bridge sandwich theorem.
  Weak Bridge under C1+C2+C5. Full equivalence conditions stated.

- **[`CRT_BRIDGE_HIERARCHY_v0_3.md`](CRT_BRIDGE_HIERARCHY_v0_3.md)** (CLOSED) — Bridge condition hierarchy.
  Primitive conditions: C1, C2, C5_R, C6. C3/C4 as sufficient route to C5_R.

- **[`CRT_TRACE_COMPLETENESS_CHARACTERIZATION_v0_2.md`](CRT_TRACE_COMPLETENESS_CHARACTERIZATION_v0_2.md)** (CLOSED) — Theorem TC:
  C6 $\iff$ GlobalCoverage under C1 + $\mathcal{D}_T^{int}$ trace semantics.

---

*See [`papers/robustness/`](../robustness/) for Mixed L2, Execution Layer, and NAA theorem files.*
