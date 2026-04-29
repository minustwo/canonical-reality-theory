# Canonical Reality Theory (CRT)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19871473.svg)](https://doi.org/10.5281/zenodo.19871473)

Canonical Reality Theory is an ongoing research program. This repository
contains preprints, technical reports, proof supplements, interface
specifications, and executable verification artifacts.

> **Status**: preprint / technical-report archive. Not all documents are
> peer-reviewed publications. "Sealed" and "Closed" denote version-locked
> internal audit states within this research archive; they do not imply
> peer-reviewed publication.

---

## Core question

When is a system justified in treating a world as canonical?
A world is canonical in CRT only when three axes align:

- **Correctness** — structurally admissible
- **Robustness** — valid justification, resistant to source-layer attack
- **Stability** — selected or maintained by the system over time

Central bridge theorem:

$$\mathrm{TracedSCSet}_T(\Pi)
  \subseteq_{\mathrm{C1+C2}}
  \mathrm{UnbreakSet}_T(\Pi)
  \subseteq_{\mathrm{C5_R}}
  \mathrm{SCSet}_T(\Pi)$$

Full equivalence requires trace-completeness ($\mathrm{SCSet} \subseteq \mathrm{CertReach}$).
When all degrees of freedom vanish:

$$\mathrm{DoF}(P) = (0,0,0)
  \iff \mathrm{SC}_T(P) = 1
  \iff C_{\min}(P) = +\infty
  \iff \mathrm{Stable}_{\mathcal{A}}(P) = 1$$

---

## Architecture

MST and IET are independent theories that CRT connects. They retain their own names.

| Layer | Question | Module | Core object |
|---|---|---|---|
| Structure | Which worlds are admissible? | MST | $\mathcal{P}_T(\Pi)$, $D_{\mathrm{comp}}$, SCSet |
| Justification | Why is a world admissible? | CRT Stack Layer 2 | $\mathcal{J}_{\mathrm{valid}}$ |
| Robustness | What breaks a justification? | Attack / Escape / Defense / Institution | $C_{\min}$, $\Delta C_{\min}$ |
| Bridge | When do SC, Unbreak, TracedSC align? | CRT Bridge Theorem | SCSet = UnbreakSet = TracedSCSet |
| Dynamics | Will agents adopt the canonical world? | IET | Stochastic stability |
| Open systems | What happens under external input? | IET-open, Escape Geometry | $C_{\min}^{\mathrm{mix}}$ |
| Execution | Where is the real control cut? | Execution Layer Min-Cut | $C_{\min}^{\mathrm{ctrl}}$ |

```
Canonical Reality Theory (CRT)
│
├── Part I.    Structure      — MST
├── Part II.   Justification — CRT Stack (Layer 2)
├── Part III.  Robustness    — Attack / Escape / Defense / Institution
├── Part IV.   Bridge        — CRT Bridge Theorem
├── Part V.    Dynamics      — IET
├── Part VI.   Open systems  — IET-open, Open-IET, Escape Geometry
└── Part VII.  Applications  — ICT CRT, DeFi CRT, Execution Layer
```

---

## Publication status

This repository is at the preprint / technical-report stage.

**Peer-reviewed publications:** none yet.

**Submitted manuscripts:**
- *Iterative Drift in DeFi Protocols* — submitted CCS 2026, under review
- *MST Probe Design for LLM Systems* — submitted arXiv
- *Multi-Step Safety in DeFi* — submitted arXiv
- *Determinization in Structure Theories* — submitted arXiv

**Technical reports and proof supplements:**
- CRT Bridge Theorem — Final Form (version-locked)
- CRT Bridge Hierarchy — SCSet = UnbreakSet = TracedSCSet (version-locked)
- CRT Representation Theorem (version-locked)
- CRT Completion Operator Theorem (version-locked)
- CRT Condition Independence (version-locked)
- CRT Mixed Layer-2 Robustness (version-locked)
- CRT Execution Layer Min-Cut Extension (version-locked)
- *CRT and Bridge Theorem Proofs* — proof supplement, [Zenodo 10.5281/zenodo.19871473](https://doi.org/10.5281/zenodo.19871473)

**Preprint:**
- *When Correctness, Robustness, and Stability Coincide* — [Zenodo 10.5281/zenodo.19871473](https://doi.org/10.5281/zenodo.19871473)

---

## Repository contents

```
canonical-reality-theory/
├── paper/          LaTeX source of synthesis paper
│   ├── main.tex
│   └── latex/        Section files + refs.bib
└── proofs/
    └── INDEX.md      Bridge Hardening Index v1.0
```

Related repositories:
- [`minustwo/market-structure-theory`](https://github.com/minustwo/market-structure-theory) — MST + CRT Bridge source (public)
- IET (Inferential Equilibrium Theory) — manuscript in preparation

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

---

## License

Documents and proof supplements: [CC BY 4.0](LICENSE-CC-BY-4.0)
Code and verification artifacts: [MIT](LICENSE-MIT)
