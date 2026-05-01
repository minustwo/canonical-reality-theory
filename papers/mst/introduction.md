# 1. Introduction
Many formal systems admit multiple internally consistent interpretations under a fixed set of constraints. This phenomenon appears across domains: logical systems with non-unique models, decision systems with multiple admissible outcomes, and structured reasoning frameworks where different conclusions satisfy the same rules. We refer to this phenomenon as plurality of admissible interpretations.
In such settings, a central problem arises:
> When, and under what conditions, can a system reduce plural admissible interpretations to a single, stable outcome?
We call this the determinization problem.
## Motivation
Plurality is not inherently pathological. In many contexts, multiple admissible interpretations reflect genuine structural ambiguity or incomplete information. However, in systems that require consistent downstream behavior, unresolved plurality can introduce instability.
A system that admits multiple interpretations without a principled way to select among them may exhibit:
- inconsistent outputs across equivalent inputs
- sensitivity to representation or ordering effects
- failure to maintain invariants under composition
These issues motivate the need for a structural understanding of when plurality can be reduced, and when it cannot.
## Scope
This work studies determinization at the level of structure theories.
A structure theory is understood, informally, as a system consisting of:
- a space of possible interpretations
- a set of constraints
- an inference or admissibility policy
We focus on the family of admissible interpretations induced by such a system.
The goal is not to optimize over interpretations, nor to assign probabilistic weights, but to analyze:
> the structural conditions under which a unique or selected interpretation may emerge.
## Types of plurality
We distinguish between at least two sources of non-determinism:
- structural plurality, arising from the underlying constraint system itself
- epistemic plurality, arising from incomplete or evolving information
This distinction is important because the mechanisms required to address each type may differ.
This work does not assume that all plurality can or should be eliminated.
## The determinization problem
We formulate the determinization problem as follows:
Given a structure theory with a non-singleton set of admissible interpretations, identify conditions under which the system admits a determinized outcome.
A determinized outcome may take different forms:
- a unique interpretation
- a selected representative under additional structure
- a reduced family satisfying stronger constraints
We do not assume that determinization is always possible.
## Contributions
This work makes the following contributions at a structural level:
1. It provides a framework for analyzing admissible interpretation families in structure theories.
2. It distinguishes different sources of plurality and their implications.
3. It formulates the determinization problem in a general structural setting.
4. It identifies conditions under which determinization may occur.
5. It characterizes limitations and failure cases where determinization does not hold.
These contributions are stated at the level of framework and scope. They do not assert completeness.
## Relation to existing approaches
This work is related to, but distinct from, several existing lines of research:
- Classical logic and model theory study models of formal systems, but do not generally frame plurality as a determinization problem.
- Judgment aggregation studies aggregation under logical constraints, but typically assumes a voting or preference structure.
- Model selection and statistical learning select models based on performance criteria rather than structural admissibility.
Our focus is not on optimization or aggregation, but on:
> the structural conditions governing admissibility and determinization.
We do not claim equivalence with these frameworks.
## Limitations
This work does not claim:
- a complete characterization of all structure theories
- a universal determinization procedure
- applicability across all domains without additional assumptions
All results are subject to explicit conditions.
## Organization
The remainder of the paper is structured as follows:
- Section 2 introduces the structural setup and admissible interpretation families.
- Section 3 analyzes types of plurality.
- Section 4 formulates the determinization problem.
- Section 5 studies conditions under which determinization may occur.
- Section 6 discusses limitations and boundaries.
- Section 7 positions the framework relative to existing work.
- Section 8 concludes.
