# CRT Open Systems

This directory contains status pages for CRT's open-systems layer.

**Publication status**: Status / positioning pages only.
Full manuscripts are not included here.
These files are not peer-reviewed publications.

> See [`STATUS_GLOSSARY.md`](../../STATUS_GLOSSARY.md) for label definitions.

---

## Architecture

The open-systems layer extends CRT to handle structural evolution and external input:

```
CRT-SEI (abstract interface: T_t → T_{t+1})
    │
    ├── Open-IET (Linear)        forward deformation / survival
    ├── Escape Geometry          inverse / minimum-energy crossing
    └── Markov-Aligned           reversible Markov dynamics companion
```

**Former internal name**: CRT-SEI was called IET-open. Open-IET (Linear) is the
concrete linear instantiation, not a synonym for CRT-SEI.

---

## Files

- **[`CRT_SEI_STATUS.md`](CRT_SEI_STATUS.md)** — CRT Structural Evolution Interface (abstract).
- **[`OPEN_IET_LINEAR_STATUS.md`](OPEN_IET_LINEAR_STATUS.md)** — Open-IET (Linear): linear instantiation.
- **[`ESCAPE_GEOMETRY_STATUS.md`](ESCAPE_GEOMETRY_STATUS.md)** — Escape Geometry: inverse companion.
- **[`MARKOV_ALIGNED_STATUS.md`](MARKOV_ALIGNED_STATUS.md)** — Markov-Aligned: reversible Markov companion.

---

*See [`papers/foundations/`](../foundations/) for MST and IET status pages.*
