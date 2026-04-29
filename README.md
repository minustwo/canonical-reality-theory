# Canonical Reality Theory (CRT)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19871473.svg)](https://doi.org/10.5281/zenodo.19871473)

Canonical Reality Theory is a structural theory of when correctness,
robustness, and stability coincide.

This repository is a public research archive for CRT. It contains
preprint-stage manuscripts, technical reports, proof supplements,
interface specifications, and verification artifacts.

> **Status**: preprint / technical-report archive.
> Peer-reviewed publications: none yet.
> "Sealed" and "Closed" denote version-locked states within this research
> archive; they do not imply peer-reviewed publication.

---

## Core idea

CRT studies when a system is justified in treating a world as canonical:
structurally admissible, justificationally valid, robust against
source-layer attack, dynamically stable, and executable without low-cost
bypass paths.

The central bridge theorem:

$$\mathrm{TracedSCSet}_T(\Pi)
  \subseteq_{\mathrm{C1+C2}}
  \mathrm{UnbreakSet}_T(\Pi)
  \subseteq_{\mathrm{C5_R}}
  \mathrm{SCSet}_T(\Pi)$$

Full equivalence requires trace-completeness
(`SCSet ⊆ CertReach`).
When all degrees of freedom vanish simultaneously:

$$\mathrm{DoF}(P) = (0,0,0)
  \iff \mathrm{SC}_T(P) = 1
  \iff C_{\min}(P) = +\infty
  \iff \mathrm{Stable}_{\mathcal{A}}(P) = 1$$

The equivalence is a structural collapse, not a coincidence.

---

## Architecture

MST and IET retain their own names as independent theories.
CRT is the unified framework that places them.

| Part | Theory / module | Role |
|---|---|---|
| Structure | MST | Admissible worlds, `P_T(Π)`, `D_comp`, SCSet |
| Justification | CRT Layer 2 | `J_declared → J_valid` pipeline |
| Attack / Escape | CRT Layers 3–4 | Break, min-HS, `C_min` |
| Defense | CRT Layer 5 | Cost hardening, redundancy |
| Institution | CRT Layer 6 | Maintaining finite threshold over horizons |
| Bridge | CRT Bridge Theorem | TracedSCSet / UnbreakSet / SCSet |
| Dynamics | IET | Long-run adoption, stochastic stability |
| Open systems | CRT-SEI, Open-IET (Linear), Escape Geometry | Structural evolution and external input |
| Applications | ICT trading (MST instance), DeFi CRT, Execution Layer | Real system instances |

```
Canonical Reality Theory (CRT)
│
├── Part I.    Structure      — MST
├── Part II.   Justification — CRT Layer 2
├── Part III.  Robustness    — Attack / Escape / Defense / Institution
├── Part IV.   Bridge        — CRT Bridge Theorem
├── Part V.    Dynamics      — IET
├── Part VI.   Open systems  — CRT-SEI, Open-IET (Linear), Escape Geometry
└── Part VII.  Applications  — ICT trading (MST instance), DeFi CRT, Execution Layer
```

### Open systems layer

CRT-SEI (Structural Evolution Interface) is the abstract interface
specifying what must be recomputed when the structure theory itself
changes: `T_t → T_{t+1}`. Former internal name: IET-open.

Open-IET (Linear) is a concrete linear-systems instantiation of CRT-SEI,
studying finite-horizon deformation under external input:
`x_{t+1} = Ax_t + B_S u_t`.

Escape Geometry is the inverse companion to Open-IET (Linear),
computing the minimum energy required to cross the canonical boundary.

---

## Repository contents

```
canonical-reality-theory/
├── THEORY_INDEX.md          Architecture and layer map
├── PUBLICATION_STATUS.md    Submission and review status
├── STATUS_GLOSSARY.md       Status label definitions
├── CITATION.cff
├── papers/
│   ├── adapters/            Language adapter diagnostic summaries
│   ├── bridge/              Bridge theorem technical reports
│   ├── robustness/          Robustness theorem technical reports
│   ├── foundations/         MST and IET status pages
│   └── open-systems/        CRT-SEI, Open-IET, EG, Markov-Aligned status pages
└── proofs/                  Version-locked proof supplements
```

---

## Synthesis paper

**When Correctness, Robustness, and Stability Coincide**
*A Unified Framework via Degrees of Freedom and Structural Collapse*
Hai Hai Fu, 2026

- Zenodo v3: https://doi.org/10.5281/zenodo.19871473

---

## Related work

- **MST** (Market Structure Theory) — structure layer.
  Manuscript submitted; pending public availability.
  Source repo: [`minustwo/market-structure-theory`](https://github.com/minustwo/market-structure-theory)
- **IET** (Inferential Equilibrium Theory) — adoption/stability layer.
  Manuscript in preparation. Key theorem in Appendix C of the synthesis paper
  ([Zenodo 10.5281/zenodo.19871473](https://doi.org/10.5281/zenodo.19871473)).

---

## License

Text, papers, and proof documents: [CC BY 4.0](LICENSE-CC-BY-4.0)
Code and verification scripts: [MIT](LICENSE-MIT)

---

## Citation

```bibtex
@misc{fu2026crt,
  author = {Fu, Hai Hai},
  title  = {When Correctness, Robustness, and Stability Coincide},
  year   = {2026},
  doi    = {10.5281/zenodo.19871473},
  url    = {https://doi.org/10.5281/zenodo.19871473}
}
```
