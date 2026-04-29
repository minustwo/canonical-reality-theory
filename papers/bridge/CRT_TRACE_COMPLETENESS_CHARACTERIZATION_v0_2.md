> **Publication status**: Technical-report / research-archive material. Not peer-reviewed.
> **Internal status**: CLOSED. See [STATUS_GLOSSARY.md](../../STATUS_GLOSSARY.md).

# CRT Trace-Completeness Characterization — v0.2

**Date**: 2026-04-28 | **Status**: CLOSED

## C6 (trace-completeness)

$$\mathrm{C6}: \quad \mathrm{SCSet}_T(\Pi) \subseteq \mathrm{CertReach}_T(\Pi)
\iff \mathrm{SCSet}_T(\Pi) = \mathrm{TracedSCSet}_T(\Pi)$$

## GlobalCoverage

$\mathrm{GlobalCoverage}(T, \mathcal{F}, \Pi)$: for every $P \in \mathrm{SCSet}$, there exists a certified seed $P_0$ and finite certified generation order $b_1,\ldots,b_m$ of $P \setminus P_0$ such that:
1. $\exists i_k, \Gamma_k$: $\mathrm{Cert}_{i_k}(\Gamma_k, b_k)$ (C1)
2. $\Gamma_k \subseteq P_0 \cup \{b_1,\ldots,b_{k-1}\}$
3. $P_0 \cup \{b_1,\ldots,b_m\} = P$

Semantic meaning: **internally grounded theory** — every canonical world derivable from internal axioms and rules, without external uncertifiable inputs.

## Main theorem: C6 ↔ GlobalCoverage

**Theorem TC**: Under C1 + $\mathcal{D}_T^{int}$ trace semantics:

$$\boxed{\mathrm{C6} \iff \mathrm{GlobalCoverage}(T, \mathcal{F}, \Pi)}$$

*Proof (⇐)*: GlobalCoverage directly constructs traced saturation with no `uncertified_seed` tags. □

*Proof (⇒)*: C6 gives traced saturation; extract certified seed and generation order from trace. □

## Corollaries

Under C1+C2+C5+C6:
$$\mathrm{SCSet} = \mathrm{CompRepSet} = \mathrm{SFRepSet} = \mathrm{UnbreakSet} = \mathrm{TracedSCSet}$$

## NoSpurious: NDLift/Unbreak axis (not C6)

NoSpurious and GlobalCoverage are orthogonal.
ICT Fork B: NoSpurious ✓, GlobalCoverage ✗.
NoSpurious belongs to C3 (NDLift), not C6.

## Boundary table

| | GC ✓, NS ✓ | GC ✓, NS ✗ | GC ✗ (Fork B) |
|---|---|---|---|
| C6 | ✓ | ✓ | ✗ |
| RT-2 | ✓ | ✗ | ✗ |
| R3 (Mixed L2) | ✓ | ✓ | ✓ |

## Semantic summary

$$\boxed{\mathrm{GlobalCoverage} \iff \text{the theory is internally grounded}}$$

- Fork A (pure rule): GlobalCoverage ✓; Full Bridge possible
- Fork B (evidence-dependent, ICT): GlobalCoverage ✗; robustness via finite $C_{\min}$, defense, institution

*End of CRT Trace-Completeness Characterization v0.2 — CLOSED.*
