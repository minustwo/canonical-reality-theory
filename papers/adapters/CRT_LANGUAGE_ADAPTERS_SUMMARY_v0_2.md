# CRT Language Adapters — Stress Test Summary

**Version**: 0.2
**Date**: 2026-04-29

**Status**: ACCEPTED diagnostic artifact.
**Publication status**: Technical-report / research-archive material. Not peer-reviewed.
**Scope**: Adapter stress tests across 16 formal languages and systems. Not a sealed theorem file.

> Across 16 language/system domains and approximately 133 cuts, all observed
> failures fell into known or explicitly named CRT boundary classes.
> No unexpected failure mode was found.
>
> CRT adapters successfully classify tested fragments and their boundaries.

---

## Core test question

For each language or system $L$, can it supply the seven CRT adapter objects:

$$\boxed{(T,\ \mathcal{P}_T,\ \mathcal{J}_{\mathrm{declared}},\ \mathcal{J}_{\mathrm{valid}},\ \mathcal{F},\ C_{\min},\ \mathfrak{I})}$$

And at which layer does the mapping pass or reach an expected boundary?

---

## Adapter fit levels

| Level | Meaning |
|---|---|
| **Full adapter fit** | All seven objects mappable over the tested fragment |
| **Open-system adapter fit** | Full fit plus CRT-SEI / Open-IET open-system layer |
| **Institution-layer adapter fit** | Admissibility + justification + Institution Layer 6 mappable |
| **Mixed evidence-supported adapter fit** | External evidence present; finite $C_{\min} \geq \theta$; not $+\infty$ |
| **Layer-1/2 adapter fit** | Admissibility + justification mappable; robustness/dynamics not fully covered |
| **Categorical reconstruction route** | CRT objects have categorical analogs; proof routes identified |
| **Quantum extension boundary** | Classical/local CRT reaches its boundary; quantum extension required |

Boundary results are labeled **EXPECTED BOUNDARY** — correctly identifying a
boundary is a positive diagnostic outcome, not a failure.

---

## Adapter matrix (16 domains)

| Domain | Adapter fit | Key stress dimension | EXPECTED BOUNDARY |
|---|---|---|---|
| Datalog | **Full** | Rule closure, completion operator | — |
| SQL (CWA) | **Full** | Evidence completeness, CWA/OWA | OWA + negation (R0c) |
| Type theory (STLC) | **Layer-1/2** | Layer-2 justification gap | Undecidable type checking (C1) |
| Prolog/ASP (stratified) | **Full + NAA** | Negation-as-failure | Non-stratified NAF (R0c) |
| Control systems | **Open-system** | CRT-SEI + Escape Geometry | — |
| DeFi | **Mixed** | Execution-layer dominance | — |
| Legal rules | **Institution-layer** | Policy maintenance over time | Discretion / no-reason rulings (Type S, C1) |
| LLM reasoning | **Mixed** | Declared $\neq$ valid justification | Self-reflection cannot eliminate Type 3 (C1) |
| Non-monotonic logic | **Full (normal) / CJC boundary** | Justification circularity | Default cycles (CJC); no stable extension (world loss) |
| Probabilistic logic | **Mixed + extension point** | Degree-of-belief admissibility | Continuous distributions (C1) |
| Temporal logic (finite) | **Full** | $\omega$-regular Institution | Infinite-state systems (C1) |
| Concurrent systems | **Full + DAG extension** | Partial-order justification | True concurrency / DAG justification |
| CSP / MIP | **Full** | Optimality as canonicity | — |
| NLP / MTT | **Layer-1/2** | Pragmatic indeterminacy | Conversational implicature (C1) |
| Category theory | **Categorical reconstruction route** | Functorial semantics | Higher categories (C1) |
| Quantum computing | **Quantum extension boundary** | Non-local support | Entanglement / Bell violation (QNL) |

---

## Boundary taxonomy

All EXPECTED BOUNDARY results fall into one of seven classes:

| Class | Definition | Status |
|---|---|---|
| **C1 (LocalExplain)** | No computable certificate relation | Known |
| **R0c (NAA)** | Absence premise not positively certifiable | Known |
| **Type S** | No unique fixed point of $D_{\mathrm{comp}}$ | Known |
| **Fork B** | External evidence; $C_{\min} = +\infty$ not achievable | Known |
| **Execution-cut** | Execution / control path dominates | Known |
| **CJC** | Circular Justification Consistency: justification validity depends on the global extension it is part of constructing | New classical boundary |
| **QNL** | Quantum Non-Locality: classical local source-node model insufficient for entangled quantum systems | Extension boundary |

**CJC** is a new classical boundary discovered in this suite. It is distinct
from R0c: R0c fails because absence is not finitely certifiable; CJC fails
because justification validity is globally circular. These are orthogonal conditions.

**QNL** is an extension boundary, not an unexpected failure of CRT core.
Current CRT is classical/local support-graph CRT
($B_T \cap \mathrm{At}_T = \emptyset$, $J \subseteq N_T \times \mathrm{At}_T$).
Quantum entanglement and Bell inequality violations require a non-local
source extension. Post-measurement systems recover classical CRT fully.

---

## Main results

**Layer-2 gap is the most universal finding**:
$$P \in \mathcal{P}_T(\Pi) \not\Rightarrow \exists J_{\mathrm{valid}}$$
Instantiated in 15 of 16 tested domains (Datalog being the clean exception
under CWA).

**Five new cross-domain connections**:
- Gricean Quality maxim (NLP) = Layer-2 $\mathrm{EV}_C$
- Adámek-style $F^\omega$ construction = candidate categorical route for MST's completion operator
- LP duality (CSP/MIP) = polynomial-time $C_{\min}$ lower bound
- LTL liveness (Temporal) = Institution Layer 6 in $\omega$-regular form
- Quantum error correction threshold $\leftrightarrow$ IET $\varepsilon_{\mathrm{eff}} = \varepsilon^k$ (conjectural connection, not proved theorem)

**CRT-SEI O3 (structural evolution) in five independent domains**:
Control systems ($A$ matrix update), SQL (schema evolution), Legal (legislation),
Temporal logic (model update), CSP (constraint addition).

---

## LLM reasoning adapter note

The LLM reasoning adapter maps P4's hallucination taxonomy to CRT Layer-2:

$$\text{hallucination} = J \in \mathcal{J}_{\mathrm{declared}} \setminus \mathcal{J}_{\mathrm{valid}}$$

This is an **adapter finding / empirical alignment**, not a proved CRT theorem.
The P4 depth gradient (surface $\to$ mid $\to$ deep constraint levels) maps
naturally to CRT layer stratification. The connection between multi-agent
error reduction ($\varepsilon_{\mathrm{eff}} = \varepsilon^k$) and IET IE-4
is a conjectural bridge, not a proved result.

---

## Statistics

| | Count |
|---|---|
| Domains tested | 16 |
| Total cuts | ~133 |
| PASS | ~117 |
| EXPECTED BOUNDARY | ~17 |
| Unexpected failures | **0** |
| New boundary classes | 1 (CJC) |
| Extension boundaries | 1 (QNL) |

---

## Related documents

- CRT Stack Interface v0.2 — Layer 0–6 definitions
- CRT Bridge Hierarchy v0.3 — Weak Bridge / Full Bridge conditions
- CRT NAA Reformulation Theorem v0.2 — bounded NAA scope
- CRT Mixed Layer-2 Robustness v0.2 — finite $C_{\min}$ threshold
- CRT Execution Layer Min-Cut v0.2 — $C_{\min}^{\mathrm{break}}$ vs $C_{\min}^{\mathrm{ctrl}}$
- Full cut suites: available in research archive (private repository)

---

*CRT Language Adapters Stress Test Summary v0.2. 2026-04-29.*
*ACCEPTED diagnostic artifact. Not a sealed theorem file. Not peer-reviewed.*
