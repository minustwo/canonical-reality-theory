# Open Systems — Status Page

**Role in CRT**: Open systems layer (CRT Part VI)

**Publication status**: Manuscripts in preparation / release-ready. Not peer-reviewed.

---

## Three components

The CRT open-systems layer has three components with distinct roles:

### CRT-SEI — Structural Evolution Interface

**What it is**: The abstract interface specifying what must be recomputed
when the structure theory itself changes: $T_t \to T_{t+1}$.

**Core question**: When $T$ evolves (new rules, new sources, changed admissibility),
which CRT objects ($C_{\min}$, $\mathcal{J}_{\mathrm{valid}}$, SCSet, etc.)
became stale and must be recomputed?

**CRT-SEI defines three event types**:
- **O1**: Evidence-only update ($T$ fixed, $\Pi_t \to \Pi_{t+1}$)
- **O2b**: Source-space expansion ($B_T$ expands, e.g., adding an execution layer)
- **O3**: Structural theory update ($T_t \to T_{t+1}$, full recomputation required)

> *Former internal name*: IET-open. Current canonical name: CRT-SEI.

---

### Open-IET (Linear)

**What it is**: A concrete linear-systems instantiation of CRT-SEI.
Studies finite-horizon deformation of the canonical basin under external input:
$$x_{t+1} = Ax_t + B_S u_t$$

**Core results**:
- **Survival test** (T1–T5): given external input $u$, does $x$ remain in $\mathcal{C}$?
- **Markov-Aligned Drift (MAD)**: sufficient condition for canonical basin stability
  under stochastic input
- **Tight displacement bound**: $r_T^2 / \mathrm{EC}_T^{\mathrm{exact}}(S)^2$

**Relationship to CRT-SEI**: Open-IET (Linear) is a specific model instantiating
CRT-SEI. CRT-SEI specifies the interface; Open-IET (Linear) is a linear implementation.

---

### Escape Geometry

**What it is**: The inverse companion to Open-IET (Linear). Rather than asking
"does the system survive given input $u$?", it asks:
$$\min \|u\|^2 \text{ such that } x \text{ exits } \mathcal{C}$$

**Core result**: Minimum escape energy
$$C_{\min}^{\mathrm{escape}} = \frac{r_T^2}{\mathrm{EC}_T^{\mathrm{exact}}(S)^2}$$

This is the tight displacement bound: the minimum energy required to cross
the canonical boundary.

**Relationship to $C_{\min}$**: Escape Geometry provides the continuous-system
analog of CRT's min-cut $C_{\min}$ in the open-system setting.

---

## Forward / Inverse duality

| | Question | Answer |
|---|---|---|
| **Open-IET (Linear)** | Given $u$, does $x$ survive? | Survival conditions T1–T5 |
| **Escape Geometry** | Min $\|u\|$ to escape $\mathcal{C}$? | $r_T^2 / \mathrm{EC}_T^2$ |

These are dual: Open-IET is forward (given input, test safety);
Escape Geometry is inverse (minimize input to break safety).

---

## Publication status

| Component | Status |
|---|---|
| CRT-SEI specification | Internal technical report (FROZEN v0.2) |
| Open-IET (Linear) | Manuscript release-ready; submission target CDC / IEEE TCNS / TAC |
| Escape Geometry | Manuscript release-ready; submission target CDC / IEEE TCNS / TAC |
| Peer-reviewed | None yet |

---

*Open Systems Status Page. 2026-04-29.*
*CRT-SEI = Structural Evolution Interface (former: IET-open).*
*Open-IET (Linear) and Escape Geometry: release-ready, not yet submitted.*
