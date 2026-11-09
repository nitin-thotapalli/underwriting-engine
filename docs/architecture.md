# Underwriting Engine — Proposed Architecture

**Status:** Exploratory investment-research design. Nothing here is a tested valuation, deployed service, regulated underwriting system or trading engine.

## Product boundary

**Evaluate the underlying asset and the supporting investment thesis.** The work is closest to capital-markets due diligence, not loan or insurance approval. Contract payoff, Greeks and portfolio optimization sit principally in the separate F&O Analyst concept.

```text
Underlying asset + investment horizon + explicit thesis
                            ↓
         Evidence intake (filings, prices, business / index context)
                            ↓
     Source validation + date/unit reconciliation + missing-data log
                            ↓
     Driver mapping and fundamental / market scenario assumptions
                            ↓
  Thesis checks (supporting / contrary evidence, catalysts, invalidators)
                            ↓
       Conditional valuation or scenario range + risk register
                            ↓
          Human-reviewed asset & thesis assessment memo
                            ↓
   Optional, future handoff to F&O Analyst (not built or required)
```

## Modules and their outputs

| Module | Inputs | Artifact / requirement |
| --- | --- | --- |
| Intake | Ticker, asset type, jurisdiction, horizon, thesis, decision context | Precisely scoped research question |
| Evidence registry | Primary filings, official exchange data, reports | Dated, classified facts with links and reviewer notes |
| Data reconciliation | Units, reporting periods, identifiers and conflicting observations | Verified dataset and exception log |
| Driver analysis | Stock/company value chain or index composition/market drivers | Observable mechanisms affecting the asset |
| Scenario/valuation model | Validated cash-flow/earnings/market assumptions where appropriate | Transparent base/bull/bear cases; sensitivity, not false precision |
| Thesis review | Supporting and contradicting evidence, risks and catalysts | Falsifiable thesis, unknowns, explicit invalidators |
| Human decision memo | Outputs of all prior stages | Conditional conclusion and follow-up questions |
| Optional interface | Reviewed research packet | An explainable summary; no unsupported AI numeric claims |

## Financial and market distinction

**Price** is observed at a timestamp. **Estimated intrinsic or fundamental value** is conditional on a chosen model and assumptions. **Futures or options theoretical value** is calculated using instrument-specific inputs. A conclusion about one does not directly prove another.

For **individual companies**, evaluate financial statements alongside operating drivers and industry structure. For **indexes**, use constituent weights, sector earnings, rates and liquidity/market context instead of pretending a single-company DCF applies.

## Validation and safety requirements

1. Every material quantitative claim is traceable to dated evidence and a reconciled unit/period.
2. Distinguish sourced fact, derived arithmetic, model output and opinion in the memo.
3. Require both supporting and contradictory evidence or mark evidence insufficient.
4. Sensitivities must span the largest uncertain assumptions, including severe downside.
5. Record missing data and invalidate unsupported conclusions rather than hallucinate facts.
6. No external trades, auto-approvals, applicant credit scores or broker access.
7. For any future handoff, share a human-reviewed **thesis packet**, never an automatic trade command.

## First proof of value

Pick a single stock or index and a hypothetical investment thesis; complete a manual reference memo first. Then reproduce the source collection, scenario calculations and risk register in a notebook. Compare the two for traceability, correctness, repeatability and time taken.

## Open architectural decisions

- Stock first or index first? What evidence is essential at the selected horizon?
- When is a fundamental value estimate appropriate and when is scenario analysis enough?
- What does a human reviewer need to overturn or reject the thesis?
- Which parts are deterministic calculations versus narrative support?
- Is an application necessary, or is a documented notebook a better first artifact?
