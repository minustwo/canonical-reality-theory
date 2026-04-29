# Market Structure Theory (MST)

**Status**: Foundational component of CRT.
**Publication status**: Preprint / submitted. Not peer-reviewed. SSRN 6582699.
**Full manuscript**: Not included in this repository.

---

## Role in CRT

MST is the **structure layer** of CRT. It defines:

- Structure theories $T = (\Sigma, A, \mathcal{I})$
- Admissible worlds $\mathcal{P}_T(\Pi)$
- Completion operator $D_{\mathrm{comp}} = F^\omega$
- Structural canonicality: $\mathrm{SC}_T(P) = 1$
- Structural canonical set: $\mathrm{SCSet}_T(\Pi) = \mathrm{Fix}(D_{\mathrm{comp}}|_{\mathcal{P}_T^+(\Pi)})$

## CRT dependency

The CRT Bridge Theorem uses MST objects directly:

$$\mathrm{TracedSCSet}_T(\Pi)
\subseteq_{\mathrm{C1+C2}}
\mathrm{UnbreakSet}_T(\Pi)
\subseteq_{\mathrm{C5_R}}
\mathrm{SCSet}_T(\Pi)$$

CRT Layer 2 extends MST by adding the justification pipeline
$\mathcal{J}_{\mathrm{declared}} \to \mathcal{J}_{\mathrm{valid}}$ on top of MST's admissibility structure.

## ICT instance

ICT (Institutional Canonicalization Theory) is the primary MST instance studied in this
research archive. It instantiates $T$ with financial market microstructure operators
(FVG detection, BOS classification, liquidity level identification).

## Related

- CRT Bridge Theorem Final v1.0.1: [`papers/bridge/CRT_BRIDGE_THEOREM_FINAL_v1_0_1.md`](../bridge/CRT_BRIDGE_THEOREM_FINAL_v1_0_1.md)
- CRT Language Adapters Summary: [`papers/adapters/CRT_LANGUAGE_ADAPTERS_SUMMARY_v0_2.md`](../adapters/CRT_LANGUAGE_ADAPTERS_SUMMARY_v0_2.md)

---

*MST_STATUS.md. Status page only. Full manuscript not included.*
