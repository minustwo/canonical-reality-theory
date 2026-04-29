# DeFi CRT Verification — v0.4

**Date**: 2026-04-28
**Status**: **CLOSED** — first-round verification complete
**Scope**: Independent on-chain / document verification of core claims

---

## Verification status overview

| Claim | Report | Verified | Confidence |
|---|---|---|---|
| Aave CAPO amount | $27M liquidations, 34 accounts, wstETH -2.85% | ✅ Confirmed | High |
| CAPO root cause | snapshotRatio/snapshotTimestamp desync | ✅ Confirmed | High |
| Proposition 5 (zero-attacker failure) | $C_{\min}=1$ → triggers without adversary | ✅ Real-world verified | High |
| Risk Steward (Chaos Labs era) | 1-of-1 | ❌ Wrong: actually 2/2 multisig | High |
| Risk Steward (post-departure) | "1-of-1 (LlamaRisk)" | ❌ Wrong: actually 2/2 multisig | High |
| Aave a1 $C_{\min}$ root cause | Risk Steward single key | ❌ Wrong: actually AgentHub execution layer | High |
| Compound Proposal 289 | Passed; 682,191 vs 633,636 COMP; 57 addresses | ✅ Confirmed | High |
| Sky GSM Pause Delay | 24h | ✅ Confirmed (primary source) | High |
| Sky all high-risk proposals share path | Spell → Chief → GSM → MCD_PAUSE_PROXY | ✅ Confirmed | High |
| Sky SP-BEAM fast track | Exists, bypasses full Spell | ✅ Contract address confirmed | High |
| Sky ESM disabled | 2025-05 | ✅ Confirmed (primary source) | High |
| a16z 20M UNI withdrawal | 2025-06, FFG Thread | ⚠️ Cannot independently verify | Low |

---

## 1. Aave CAPO event — ✅ Confirmed

$27M, 34 accounts, 10,938 wstETH, 2.85% undervaluation (1.1939 vs 1.228), 499 ETH bot revenue, no bad debt, full restitution.

Root cause: `snapshotRatio` and `snapshotTimestamp` pushed asynchronously by BGD AgentHub automated pipeline without human review buffer.

**Proposition 5 verified**: No adversary; misconfigured automated push triggered $27M liquidations.

**Execution layer insight** (see `CRT_EXECUTION_LAYER_v0_1.md`): Aave a1 $C_{\min} = 1$ comes from the execution layer (AgentHub pipeline), not the protocol layer (Risk Steward 2/2 multisig). Audit report numerical value correct; causal attribution wrong.

---

## 2. Risk Steward configuration — ❌ Major correction

**Primary source**: LlamaRisk ARFC (2026-04-09):
> "Risk Council multisigs **(2/2, on all instances)**... @AaveLabs + @LlamaRisk"

- Chaos Labs era: 2/2 (Chaos Labs + BGD Labs)
- Post-departure: 2/2 (LlamaRisk + Aave Labs)
- AIP 284 Phase 3: parameter-range expansion only; does not modify signer configuration

$C_{\min}^{ctrl,proto}(\text{Risk Steward}) = 2$, but $C_{\min}^{ctrl,exec}(\text{AgentHub}) = 1$, so $C_{\min}(\text{a1}) = 1$ is execution-layer dominated. Proposition 2 (fast-path dominance) still holds.

---

## 3. Compound Proposal 289 — ✅ Confirmed

682,191 vs 633,636 COMP; 57 addresses; 499,000 COMP $\approx$ $24M; passed 2024-07-28; no Proposal Guardian at time of P289 (introduced in P303, August 2024). $C_{\min}^{ctrl,proto} = 1$ at time of event confirmed.

---

## 4. Sky Chief hat path — ✅ Confirmed

All six high-risk action types (contract upgrades, Treasury, stability fees, Collateral, SubDAO, modify GSM delay itself) route through:
$$\text{Spell} \to \text{Chief V3 hat} \to \text{MCD\_PAUSE} \to \text{MCD\_PAUSE\_PROXY}$$

GSM Pause Delay = 24h. SP-BEAM (`0x36B072...`, deployed 2025-04-17): execution-layer fast track, $C_{\min}^{ctrl,exec} = 1$. ESM disabled 2025-05-15. Office-hours: Mon–Fri 14:00–21:00 UTC.

---

## 5. CRT framework proposition verification

| Proposition | Content | Status |
|---|---|---|
| P1 (Min-cut defense principle) | $C_{\min}$ determined by shortest break path | ✅ CAPO empirically verified |
| P2 (Fast-path dominance) | Corrected: exec ≤ fast-path < main | ✅ Verified (with layer correction) |
| P3 (Shared root centrality collapse) | Shared root → centrality = 1 | ✅ Sky Case A confirmed |
| P5 (Zero-attacker failure) | $C_{\min}=1$ → ops error sufficient | ✅ CAPO real-world verified |

---

## 6. Audit report errors

| Error | Severity | Correction |
|---|---|---|
| Risk Steward always 2/2 multisig, not 1-of-1 | **High** | LlamaRisk: "2/2 on all instances" |
| Post-departure: 2/2 (not 1-of-1) | **High** | Primary source confirmed |
| AIP 284 Phase 3 cited as signer config source | **High** | AIP 284 = parameter-range expansion only |
| Aave a1 $C_{\min}=1$ attributed to Risk Steward | **High** | Correct: AgentHub execution layer; number right, mechanism wrong |
| a16z 20M UNI withdrawal cites FFG Thread | **Medium** | FFG Thread does not contain this event |

---

## 7. New theoretical contribution from verification

Verification produced a new CRT layer-transition insight, formalized in `CRT_EXECUTION_LAYER_v0_1.md`:

$$C_{\min}(a) = \min\left(C_{\min}^{gov}, C_{\min}^{proto}, C_{\min}^{exec}\right)$$

CAPO proves the execution layer can be the true minimum cut regardless of governance/protocol layer thickness. Upgrades Proposition 2 from "fast-path dominates main" to "execution layer dominates all layers."

---

*End of DeFi CRT Verification v0.4 — CLOSED.*
*✅ Confirmed: CAPO event, Compound P289, Sky full path, SP-BEAM, ESM.*
*❌ Corrected: Risk Steward 2/2 multisig; execution layer as true $C_{\min}$ source; FFG Thread citation error.*
*⚠️ Unverified: Uniswap a16z 20M UNI specific figure.*
