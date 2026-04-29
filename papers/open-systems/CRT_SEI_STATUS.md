# CRT Structural Evolution Interface (CRT-SEI)

**Former internal name**: IET-open.
**Status**: Interface / status page.
**Publication status**: Technical-report status. Not peer-reviewed.

---

## Role

CRT-SEI specifies the **recomputation contract** when the structure theory itself evolves:

$$T_t \to T_{t+1}$$

It defines what must be recomputed in the CRT Stack when the underlying structure theory
changes — new atom types, new operators, new admissibility rules.

## Event taxonomy (O1–O3)

| Event | Description |
|---|---|
| O1 | Atom-type addition / removal |
| O2a | Operator parameter update (within existing operator family) |
| O2b | New operator / source node addition |
| O3 | Admissibility rule change |

O2b (new source node insertion) is the CRT-SEI classification of execution-layer
insertion events (e.g., adding AgentHub to an existing DeFi protocol).

## Relationship to Open-IET (Linear)

CRT-SEI is the **abstract interface**. Open-IET (Linear) is a **concrete instantiation**
of CRT-SEI using linear dynamical systems:

$$x_{t+1} = Ax_t + B_S u_t$$

They are not synonyms. CRT-SEI applies to any structure-theory evolution;
Open-IET (Linear) is specific to finite-horizon linear deformation.

## Naming note

The former internal name IET-open referred to the abstract structural evolution interface.
The current canonical name is **CRT-SEI**. Open-IET (Linear) retains its name as the
linear instantiation.

---

*CRT_SEI_STATUS.md. Status page only.*
