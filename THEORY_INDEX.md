# CRT Theory Index

## Name

Canonical Reality Theory (CRT)

**Tagline**: A structural theory of when correctness, robustness, and stability coincide.

---

## Core question

> When do correctness, robustness, and stability describe the same state?

A world $P$ is canonical in CRT only when all three axes align:
- **Correctness** — structurally admissible ($\mathrm{SC}_T(P) = 1$)
- **Robustness** — source-layer unbreakable ($C_{\min}(P) = +\infty$)
- **Stability** — dynamically selected ($\mathrm{Stable}_{\mathcal{A}}(P) = 1$)

---

## Architecture

| Part | Theory / module | Core question | Core object |
|---|---|---|---|
| Structure | MST | Which worlds are admissible? | $\mathcal{P}_T(\Pi)$, $D_{\mathrm{comp}}$, SCSet |
| Justification | CRT Layer 2 | Why is a world admissible? | $\mathcal{J}_{\mathrm{declared}} \to \mathcal{J}_{\mathrm{valid}}$ |
| Attack / Escape | CRT Layers 3–4 | What breaks a justification? | $\mathrm{Break}$, min-HS, $C_{\min}$ |
| Defense | CRT Layer 5 | How can robustness be raised? | $\delta$, $\Delta C_{\min}$ |
| Institution | CRT Layer 6 | How is validity maintained over time? | $\iota$, threshold floor |
| Bridge | CRT Bridge Theorem | When do SC, Unbreak, TracedSC align? | SCSet = UnbreakSet = TracedSCSet |
| Dynamics | IET | Will agents adopt the canonical world? | Stochastic stability, $P^{\mathrm{canon}}$ |
| Open systems | CRT-SEI, Open-IET (Linear), Escape Geometry | What happens under structural evolution and external input? | $C_{\min}^{\mathrm{mix}}$, escape energy |
| Applications | ICT CRT, DeFi CRT, Execution Layer | Where is the real minimum cut? | $C_{\min}^{\mathrm{ctrl}}$ |

**Open systems layer**:
- **CRT-SEI** (Structural Evolution Interface) — abstract interface for $T_t \to T_{t+1}$ evolution. Former internal name: IET-open.
- **Open-IET (Linear)** — linear-systems instantiation of CRT-SEI.
- **Escape Geometry** — inverse minimum-energy crossing companion to Open-IET (Linear).

---

## Central results

**Bridge Sandwich** (Weak Bridge, SEALED v1.0.1):
$$\mathrm{TracedSCSet}_T(\Pi)
  \subseteq_{\mathrm{C1+C2}}
  \mathrm{UnbreakSet}_T(\Pi)
  \subseteq_{\mathrm{C5_R}}
  \mathrm{SCSet}_T(\Pi)$$

**Full Bridge** (under C1+C2+C5_R+C6):
$$\mathrm{SCSet}_T(\Pi) = \mathrm{UnbreakSet}_T(\Pi) = \mathrm{TracedSCSet}_T(\Pi)$$

**Synthesis Theorem** (DoF collapse):
$$\mathrm{DoF}(P)=(0,0,0)
  \iff \mathrm{SC}_T(P)=1
  \iff C_{\min}(P)=+\infty
  \iff \mathrm{Stable}_{\mathcal{A}}(P)=1$$

**Execution Layer** (EL-1B):
$$C_{\min}^{\mathrm{ctrl},exec} \leq C_{\min}^{\mathrm{ctrl},proto} \leq C_{\min}^{\mathrm{ctrl},gov}$$

---

## Technical reports (public)

### Bridge core

| Document | Version | Status | Link |
|---|---|---|---|
| CRT Bridge Theorem — Final Form | v1.0.1 | **SEALED** | [`papers/bridge/CRT_BRIDGE_THEOREM_FINAL_v1_0_1.md`](papers/bridge/CRT_BRIDGE_THEOREM_FINAL_v1_0_1.md) |
| CRT Bridge Hierarchy | v0.3 | **CLOSED** | [`papers/bridge/CRT_BRIDGE_HIERARCHY_v0_3.md`](papers/bridge/CRT_BRIDGE_HIERARCHY_v0_3.md) |
| CRT Trace-Completeness Characterization | v0.2 | **CLOSED** | [`papers/bridge/CRT_TRACE_COMPLETENESS_CHARACTERIZATION_v0_2.md`](papers/bridge/CRT_TRACE_COMPLETENESS_CHARACTERIZATION_v0_2.md) |

### Robustness core

| Document | Version | Status | Link |
|---|---|---|---|
| CRT Mixed Layer-2 Robustness | v0.2 | **CLOSED** | [`papers/robustness/CRT_MIXED_L2_ROBUSTNESS_v0_2.md`](papers/robustness/CRT_MIXED_L2_ROBUSTNESS_v0_2.md) |
| CRT Execution Layer Min-Cut | v0.2 | **CLOSED** | [`papers/robustness/CRT_EXECUTION_LAYER_MINCUT_v0_2.md`](papers/robustness/CRT_EXECUTION_LAYER_MINCUT_v0_2.md) |
| CRT NAA Reformulation Theorem | v0.2 | **CLOSED** | [`papers/robustness/CRT_NAA_REFORMULATION_THEOREM_v0_2.md`](papers/robustness/CRT_NAA_REFORMULATION_THEOREM_v0_2.md) |

> "Sealed" = version-locked; "Closed" = version-locked after final audit pass.
> Neither implies peer-reviewed publication.
> See [`STATUS_GLOSSARY.md`](STATUS_GLOSSARY.md) for full definitions.

---

## Diagnostic artifacts

| Document | Version | Status | Link |
|---|---|---|---|
| CRT Language Adapters Summary | v0.2 | Accepted diagnostic artifact | [`papers/adapters/CRT_LANGUAGE_ADAPTERS_SUMMARY_v0_2.md`](papers/adapters/CRT_LANGUAGE_ADAPTERS_SUMMARY_v0_2.md) |
| CRT Vertical Stress Test Summary | v0.1 | Accepted diagnostic artifact | [`papers/adapters/CRT_VERTICAL_STRESS_TEST_SUMMARY_v0_1.md`](papers/adapters/CRT_VERTICAL_STRESS_TEST_SUMMARY_v0_1.md) |

These are stress-test reports, not theorem files. See [`papers/adapters/README.md`](papers/adapters/README.md).

---

## Foundations status pages

| Theory | Role | Status page |
|---|---|---|
| MST | Structure layer | [`papers/foundations/MST_STATUS.md`](papers/foundations/MST_STATUS.md) |
| IET | Dynamics layer | [`papers/foundations/IET_STATUS.md`](papers/foundations/IET_STATUS.md) |
| Open systems (CRT-SEI, Open-IET, EG) | Open systems layer | [`papers/foundations/OPEN_SYSTEMS_STATUS.md`](papers/foundations/OPEN_SYSTEMS_STATUS.md) |

---

## Companion document

*CRT and Bridge Theorem Proofs* — proof supplement:
- Appendix A: Bridge Hierarchy full proof
- Appendix B: EL-1A / EL-1B (Execution Layer)
- Appendix C: IET Endogenous Canonical Selection

Zenodo: https://doi.org/10.5281/zenodo.19871473
