# Canonical Reality Theory (CRT)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19871473.svg)](https://doi.org/10.5281/zenodo.19871473)

Canonical Reality Theory studies when a system is justified in treating
a world as canonical.
A world is canonical in CRT only when three axes align:

- **Correctness**: it is structurally admissible.
- **Robustness**: it has valid support and nontrivial resistance to source-layer attack.
- **Stability**: it is selected or maintained by the system over time.

The central bridge theorem:

$$\mathrm{TracedSCSet}_T(\Pi)
  \subseteq_{\mathrm{C1+C2}}
  \mathrm{UnbreakSet}_T(\Pi)
  \subseteq_{\mathrm{C5_R}}
  \mathrm{SCSet}_T(\Pi)$$

Full equivalence requires trace-completeness:

$$\mathrm{SCSet}_T(\Pi) \subseteq \mathrm{CertReach}_T(\Pi)$$

When all degrees of freedom vanish, the three notions collapse into one:

$$\mathrm{DoF}(P) = (0,0,0)
  \iff \mathrm{SC}_T(P) = 1
  \iff C_{\min}(P) = +\infty
  \iff \mathrm{Stable}_{\mathcal{A}}(P) = 1$$

---

## Architecture

CRT is organized into five layers. MST and IET retain their own names as
independent theories; CRT is the unified framework that connects them.

| Layer | Question | Module | Core object |
|---|---|---|---|
| Structure | Which worlds are admissible? | MST | $\mathcal{P}_T(\Pi)$, $D_{\mathrm{comp}}$, SCSet |
| Justification | Why is a world admissible? | CRT Stack Layer 2 | $\mathcal{J}_{\mathrm{valid}}$ |
| Robustness | What breaks a justification? | Attack/Escape, Defense, Institution | $C_{\min}$, $\Delta C_{\min}$ |
| Bridge | When do SC, Unbreak, TracedSC align? | CRT Bridge Theorem | SCSet = UnbreakSet = TracedSCSet |
| Dynamics | Will agents adopt the canonical world? | IET | Stochastic stability, $P^{\mathrm{canon}}$ |
| Open systems | What happens under external input? | IET-open, Open-IET, Escape Geometry | $C_{\min}^{\mathrm{mix}}$, escape energy |
| Execution | Where is the real control cut? | Execution Layer Min-Cut | $C_{\min}^{\mathrm{ctrl}}$ |

```
Canonical Reality Theory (CRT)
│
├── Part I.   Structure          — MST
├── Part II.  Justification      — CRT Stack (Layer 2)
├── Part III. Robustness         — Attack/Escape, Defense, Institution
├── Part IV.  Bridge             — CRT Bridge Theorem
├── Part V.   Dynamics           — IET
├── Part VI.  Open systems       — IET-open, Open-IET, Escape Geometry
└── Part VII. Applications       — ICT CRT, DeFi CRT, Execution Layer
```

---

## Synthesis paper

**When Correctness, Robustness, and Stability Coincide**
*A Unified Framework via Degrees of Freedom and Structural Collapse*
Hai Hai Fu, 2026

- **Zenodo v2** (current): https://doi.org/10.5281/zenodo.19871473
- **LaTeX source**: [`paper/`](paper/)
- **Proof index**: [`proofs/INDEX.md`](proofs/INDEX.md)

---

## Related work

The underlying theories (MST, IET) are developed in separate working papers
currently under preparation. Key theorems are reproduced in the companion
document available at Zenodo (see DOI above).

- **MST** (Market Structure Theory): structure layer. SSRN 6582699.
- **IET** (Inferential Equilibrium Theory): adoption/stability layer. Manuscript in preparation.
- **CRT Bridge proofs**: companion document, [Zenodo 10.5281/zenodo.19871473](https://doi.org/10.5281/zenodo.19871473).

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
