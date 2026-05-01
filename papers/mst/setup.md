# 2. Setup
## 2.1 Informal structure of a theory
We begin by outlining the objects under consideration.
A structure theory is intended to capture systems in which conclusions are not derived uniquely, but rather selected from a family of admissible interpretations. Instead of committing to a specific formalism at the outset, we describe the components at a structural level.
A structure theory consists, informally, of:
- a space of candidate interpretations
- a collection of constraints
- a rule governing admissibility
Given such a system, we are interested in the set of interpretations that satisfy the admissibility rule.
We refer to this set as the admissible interpretation family.
This section introduces notation and terminology sufficient to reason about such families without fixing a specific formal encoding.
## 2.2 Interpretation space
Let `I` denote a space of candidate interpretations.
An interpretation should be understood as a complete assignment of structural conclusions within the system under consideration. The exact representation of interpretations is intentionally left open, as it may vary across domains.
We do not assume:
- a specific logical language
- a particular algebraic structure
- a probabilistic interpretation
The only requirement is that interpretations can be compared with respect to constraint satisfaction.
## 2.3 Constraints and admissibility
Let `C` denote a collection of constraints.
Constraints may represent:
- logical consistency requirements
- structural conditions
- domain-specific restrictions
We write that an interpretation `P in I` satisfies `C` when `P` satisfies the constraint set.
Admissibility is determined by a rule `A`, which may depend on both `C` and additional structural considerations.
We define the admissible interpretation family as:
```text
P_T subset I

where T denotes the underlying structure theory.

We do not assume that P_T is a singleton.

2.4 Admissible interpretation families

The central object of study is the set:

P_T = { P in I : P is admissible under T }

We refer to P_T as the admissible interpretation family.

This family may exhibit:

* uniqueness, when it contains exactly one element
* plurality, when it contains multiple admissible interpretations

Plurality is the primary case of interest in this work.

2.5 Non-determinism

We say that a structure theory T is:

* deterministic if |P_T| = 1
* non-deterministic if |P_T| > 1

Non-determinism does not imply inconsistency. All elements of P_T are assumed to satisfy admissibility.

The question is not whether interpretations are valid, but whether they are unique.

2.6 Determinization

We use the term determinization to refer to any process or condition under which a non-deterministic structure theory yields a reduced or selected outcome.

At this stage, we do not fix:

* a canonical selection rule
* a reduction operator
* a uniqueness criterion

Determinization may depend on:

* additional constraints
* refinement of admissibility
* structural augmentation

We treat determinization as a property to be analyzed, not assumed.

2.7 Scope and non-assumptions

We emphasize the following:

* no assumption is made that determinization is always possible
* no canonical selection mechanism is fixed at this stage
* no equivalence is assumed between different notions of determinization

This section provides only the minimal structure needed to state the determinization problem.

Further specialization should be introduced only when required.
