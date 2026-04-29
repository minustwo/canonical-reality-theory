# Markov-Aligned Channel Vulnerability

**Status**: Open-system / Markov companion.
**Publication status**: Technical report / preprint-stage. Not peer-reviewed.
**Full manuscript**: Not included in this repository.

---

## Role

Markov-Aligned Channel Vulnerability provides **computable channel-level vulnerability
scores** for reversible Markov dynamics, and links forward disagreement gain to
Escape Geometry operator gain.

## Core contribution

For a reversible Markov chain with transition matrix $P$:
- Define per-channel vulnerability score $v(c)$ from stationary distribution and mixing
- Link HS score (hitting-set cost in CRT Break/min-HS sense) to operator escape gain
- Provide computable approximation via spectral gap

## Boundary

Markov-Aligned is a **companion** to Open-IET (Linear) and Escape Geometry,
not a modification or extension of either.

| Component | Role |
|---|---|
| Open-IET (Linear) | Linear dynamics, forward survival |
| Escape Geometry | Linear dynamics, inverse minimum-energy |
| Markov-Aligned | Reversible Markov dynamics, channel vulnerability |

The HS score / operator escape gain connection provides a bridge between
the CRT Break/min-HS machinery (discrete) and the Markov mixing / spectral gap
(continuous / probabilistic).

---

*MARKOV_ALIGNED_STATUS.md. Status page only. Full manuscript not included.*
