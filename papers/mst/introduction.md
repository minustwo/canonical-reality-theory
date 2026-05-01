# 1. Introduction

Many formal systems admit multiple internally consistent interpretations under a fixed set of constraints. This phenomenon appears across domains, including logical systems with non-unique models, decision systems with multiple admissible outcomes, and structured reasoning frameworks in which different conclusions satisfy the same governing rules. We refer to this phenomenon as the plurality of admissible interpretations.

In such settings, a central question arises: when, and under what conditions, can a system reduce a plural admissible set to a single, stable outcome? We study this question as the determinization problem. The problem is structural rather than merely procedural. It concerns the conditions under which a family of admissible interpretations may support a unique interpretation, a selected representative, or a reduced admissible family under stronger requirements.

## Motivation

Plurality is not inherently pathological. In many contexts, multiple admissible interpretations reflect genuine ambiguity in the underlying structure, incomplete information, or a deliberate tolerance for alternative admissible states. At the same time, plurality can create instability in systems that require consistent downstream behavior. When a system admits multiple interpretations without a principled way to reduce or control them, it may exhibit inconsistent outputs across equivalent inputs, sensitivity to representation or ordering effects, or failure to maintain invariants under composition and extension.

These concerns motivate the need for a structural account of determinization. Rather than treating ambiguity as an isolated defect or forcing a domain-specific selection rule, we consider the more general question of when plurality can be reduced by the structure of the system itself, and when it cannot.

## Scope

This work studies determinization at the level of structure theory. Informally, a structure theory consists of a space of possible interpretations, a set of constraints, and an admissibility or inference policy that determines which interpretations count as acceptable. Our object of study is the family of admissible interpretations induced by such a system.

We do not study optimization over hypotheses, probabilistic weighting over candidates, or domain-specific performance criteria. Instead, we analyze the structural conditions under which a unique or selected interpretation may emerge from a plural admissible family. The emphasis is on admissibility, plurality, and determinization, rather than on prediction, equilibrium computation, or implementation design.

## Types of plurality

We distinguish between at least two broad sources of non-determinism. The first is structural plurality, which arises from the underlying constraint system itself. The second is epistemic plurality, which arises from incomplete, partial, or evolving information. This distinction matters because the mechanisms relevant to each case may differ. A system may remain plural because its structure permits multiple admissible interpretations, because available information is insufficient to reduce them, or because both features are present simultaneously.

We do not assume that all plurality can or should be eliminated. In some settings, plurality is a meaningful feature of the system rather than a defect. The determinization problem is therefore not the universal elimination of multiplicity, but the analysis of when and how reduction is structurally available.

## Relation to existing approaches

This work is related to, but distinct from, several established lines of inquiry. It is related to classical logic and model theory in that both study interpretations satisfying formal constraints. However, our focus is not the general study of models as such, but the structural analysis of admissible families and the conditions under which determinization may occur.

It is also related to judgment aggregation, which studies how logically constrained judgments may be combined. The present framework does not assume a voting setting, a preference aggregation problem, or an aggregation operator over agents. Its focus is the admissibility structure itself rather than the aggregation of submitted judgments.

Finally, this work is distinct from model selection and statistical learning. Those frameworks typically select among candidate models using predictive, inferential, or performance-based criteria. By contrast, we consider admissibility and determinization at the structural level, without reducing the problem to optimization over hypotheses or empirical fit.

We do not claim equivalence with any of these frameworks. The point of comparison is to clarify scope and avoid misclassification.

## Informal contribution summary

At a structural level, this work makes five contributions. First, we study a general framework for analyzing admissible interpretation families in structure theories. Second, we distinguish different sources of plurality and explain why this distinction matters for determinization. Third, we formulate the determinization problem in a general structural setting. Fourth, we analyze conditions under which determinization may occur. Fifth, we identify limitations and failure cases in which determinization does not hold or does not follow from the available structure alone.

These contributions are presented with explicit scope. They are not claims of completeness, universality, or unrestricted applicability.

## Limitations

This work does not claim a complete characterization of all structure theories, a universal determinization procedure, or applicability across all domains without additional assumptions. Any determinization result must remain sensitive to the structure under consideration, the admissibility policy in use, and the information available to the system. Our aim is to clarify the problem and its structural conditions, not to assert that plurality can always be resolved.

## Organization

The remainder of the paper is structured as follows. Section 2 introduces the structural setup and admissible interpretation families. Section 3 analyzes types of plurality. Section 4 formulates the determinization problem more precisely. Section 5 studies conditions under which determinization may occur. Section 6 discusses limitations and boundaries. Section 7 positions the framework relative to existing work. Section 8 concludes.
