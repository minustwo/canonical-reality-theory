# Canonical Reality Theory (CRT)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19871473.svg)](https://doi.org/10.5281/zenodo.19871473)

**A Structural Theory of Correctness, Robustness, and Stability**

Author: Hai Hai Fu &nbsp;|&nbsp; **Zenodo**: [10.5281/zenodo.19871473](https://doi.org/10.5281/zenodo.19871473) &nbsp;|&nbsp; **SSRN**: [6582699](https://ssrn.com/abstract=6582699)

---

## What is CRT?

Canonical Reality Theory studies a fundamental question:

> *What does it take for a system to commit to a single canonical world — one that is structurally correct, adversarially robust, and dynamically stable?*

**Main result** (Synthesis Theorem):

$$\mathrm{DoF}(P) = (0,0,0)
  \iff \mathrm{SC}_T(P) = 1
  \iff C_{\min}(P) = +\infty
  \iff \mathrm{Stable}_{\mathcal{A}}(P) = 1$$

The equivalence is not assumed. It is a structural collapse: when all degrees of freedom vanish, there is only one thing the system can be.

---

## Theory architecture

CRT is the unified theory. MST, IET, and the open-system companions are its constituent layers — each retains its own name.

```
Canonical Reality Theory (CRT)
│
├── Part I. Structure
│   └── MST (Market Structure Theory)
│       Which worlds are admissible? — Θ, P_T(Π), D_comp, SCSet
│
├── Part II. Justification and Robustness
│   ├── MST Layer 2 / CRT Layer 2
│   │   J_declared → J_valid → J* validity pipeline
│   ├── Attack / Escape
│   │   C_min, Break/min-HS
│   ├── Defense
│   │   Raise escape cost, lower source concentration
│   ├── Institution
│   │   Cross-horizon validity + threshold maintenance
│   └── CRT Bridge Theorem
│       SCSet = UnbreakSet = TracedSCSet under C1+C2+C5_R+C6
│
├── Part III. Dynamics and Adoption
│   └── IET (Inferential Equilibrium Theory)
│       If a canonical world exists, will agents adopt it?
│       P_canon is the unique stochastically stable state.
│
├── Part IV. Open Systems
│   ├── IET-open
│   │   Abstract structural evolution: T_t → T_{t+1}
│   ├── Open-IET (Linear)
│   │   Finite-horizon deformation under external input
│   └── Escape Geometry
│       Inverse escape-energy companion
│
└── Part V. Applications
    ├── ICT CRT
    ├── DeFi CRT
    └── Execution Layer Min-Cut
```

**One-line summary**:
> MST tells you what is structurally canonical. CRT Bridge tells you when it is justified and robust. IET tells you when it is selected in the long run. Open-CRT studies deformation, escape, and execution under external input.

---

## This repository

This repo contains the **synthesis paper** that connects Parts I–III:

**When Correctness, Robustness, and Stability Coincide**
*A Unified Framework via Degrees of Freedom and Structural Collapse*
Hai Hai Fu, 2026

- **Zenodo v2** (current): https://doi.org/10.5281/zenodo.19871473
- **LaTeX source**: [`paper/`](paper/)
- **Proof index**: [`proofs/INDEX.md`](proofs/INDEX.md)

---

## Related repositories

| Repo | Layer | Status |
|---|---|---|
| `minustwo/market-structure-theory` | MST + CRT Bridge source | Public |
| `minustwo/inferential-equilibrium-theory` | IET | Private (forthcoming) |
| `minustwo/canonical-reality-theory` | Synthesis paper | **Public (this repo)** |

---

## Citation

```bibtex
@misc{fu2026crt,
  author = {Fu, Hai Hai},
  title  = {When Correctness, Robustness, and Stability Coincide:
            A Unified Framework via Degrees of Freedom and Structural Collapse},
  year   = {2026},
  doi    = {10.5281/zenodo.19871473},
  url    = {https://doi.org/10.5281/zenodo.19871473}
}
```
