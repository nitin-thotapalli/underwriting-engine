# Underwriting Engine — Research & Development Roadmap

**Status:** Proposed capital-markets research experiments. Nothing has been deployed or validated.

| Gate | Deliverable | Evidence needed to continue |
| --- | --- | --- |
| 01 — Scope | One underlying asset, horizon, hypothesis and intended decision | Decision clearly separate from derivative contract selection |
| 02 — Evidence | Source register of filings/market inputs with verification dates | Material fields, units, periods and conflicts recorded |
| 03 — Driver map | Business/industry or index composition analysis | Distinguishes observed drivers from speculative explanations |
| 04 — Thesis | Supporting and contradicting evidence, catalysts, invalidators | Thesis is falsifiable and has an evidence-sufficiency test |
| 05 — Scenarios | Reproducible value or scenario range with sensitivities | Reviewer can recalculate and challenge major assumptions |
| 06 — Risk | Downside/event/liquidity risk register and critical unknowns | No major risk is silently omitted; uncertainty visible |
| 07 — Decision memo | Investigate / reject / conditional consideration | Evidence-linked reasoning with explicit human sign-off |
| 08 — Product review | Compare manual memo vs prototype for value | Time, correctness, traceability, rework and upkeep assessed |

## Initial acceptance checks

- [ ] Define **asset vs instrument** and avoid treating one price as the other.
- [ ] Use real, licensable primary references or clearly labelled test data.
- [ ] Reconcile material numbers and support all crucial assertions with sources.
- [ ] Show a downside scenario and what would invalidate the thesis.
- [ ] Present estimated values as ranges conditional on model assumptions.
- [ ] Independently review calculations and keep a change log.
- [ ] Refuse to conclude where evidence is insufficient.
- [ ] Do not connect a broker, place trades or auto-approve any transaction.

## Candidate success measures

Source traceability, independent reconciliation of facts, reproducibility of scenarios, completeness of downside risks, falsifiability of theses, and time to a reviewed memo. Compare with a manual baseline; no measured speed or investment returns have been demonstrated.

## Non-goals

Credit and insurance application processing; loan approval; regulatory policy engines; applicant scoring; live derivative order routing; full portfolio risk analytics (a separate F&O Analyst concern); guaranteed price forecasts.

## Decision to make later

Whether this is a useful stand-alone personal research workflow, whether it should remain a component of one's personal F&O research process, or whether to stop after a well-documented notebook. A commercial product is not assumed.
