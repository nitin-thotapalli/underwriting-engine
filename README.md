# Underwriting Engine

**Investigate the underlying asset. Test the investment thesis. Make risk explicit.**

Underwriting Engine is an independent research concept for **evaluating an asset or investment opportunity before taking exposure to it**. In the current direction, the first use case is to assess the **underlying asset behind a proposed futures or options position**—what drives its value, how it is performing, what could change, and what risks are not reflected in a simple market quote.

**Status:** Concept / research. No operational underwriting system, validated valuation engine, broker integration, or investment recommendation service is claimed.

## Why Underwriting Engine?

A quoted price tells me **what the market currently offers**, not necessarily **what an asset is worth, why its price is moving, or whether the risk is justified**.

Before considering a derivative position, I want to examine the underlying: the company's financial health and operations if it is a stock, or the composition, market drivers, and macroeconomic context if it is an index. Then I want to connect that assessment to the proposed exposure: **What would have to be true for this thesis to work, how could it fail, and what loss could result?**

The research process is often fragmented: filings, prices, financial statements, business drivers, valuation assumptions, event risks, and derivative contract terms live in different places. Collecting the facts is only the first challenge; separating evidence from assumptions and building a consistent decision record is the harder one.

The central question is:

**What am I actually taking exposure to, what supports the thesis, and is the potential downside acceptable under explicit assumptions?**

This project explores a structured, explainable process for answering that question. It is **investment/asset underwriting in the sense of disciplined due diligence and risk assessment**, not credit-loan or insurance-policy underwriting.

## What exactly is being evaluated?

There are **two distinct layers**, and they should not be confused.

| Layer | Key question | Example analysis |
| --- | --- | --- |
| **Underlying asset** | What drives the asset's value and performance? | Business fundamentals, cash flow, operations, industry, macro factors, valuation, catalysts |
| **Proposed exposure** | Is this particular futures/options contract or strategy an appropriate way to express a thesis? | Strike, expiry, premium, Greeks, liquidity, margin, payoff, scenario losses |

An underlying asset's **market price** is observable. Its **estimated fundamental value** requires a model, evidence, and uncertain assumptions. An option's **market premium** is observable; its **theoretical value** depends on a pricing model and inputs. None of these should be presented as interchangeable.

For a **single stock**, fundamental analysis may include revenue drivers, margins, cash generation, balance sheet, competitive position, value chain, and valuation. For an **index**, company-level valuation alone is insufficient; the relevant analysis may include constituent weights, sector exposures, aggregate earnings, rates, flows, and broader market conditions.

## Who is it for?

Initially, **me** as a research and learning tool for evaluating underlying assets and investment theses before considering derivative exposure. A later analyst-facing workflow is possible but has not been validated.

## Proposed underwriting questions

1. **Identify the exposure:** Which asset, contract, horizon, and thesis are under consideration?
2. **Understand the asset:** How does it generate value, what moves its price, and what has changed recently?
3. **Assess quality of evidence:** Which facts are verified, which data are stale or conflicting, and which statements are assumptions?
4. **Estimate value or scenarios:** What range of outcomes follows from explicit business, market, and valuation assumptions?
5. **Identify risks:** What events, financial weaknesses, operational problems, or market conditions could invalidate the thesis?
6. **Connect thesis to instrument:** Does the derivative's payoff, expiry, liquidity, and risk actually fit the underlying view?
7. **Record a decision:** What is supported, what remains unknown, and what would cause a rejection or further investigation?

## Research workflow

### 1. Intake and scope

Record the underlying asset, proposed investment or strategy, investment horizon, thesis, and personal risk constraints. Do not begin with a recommendation.

### 2. Evidence collection and verification

Gather permitted price history, filings, financial statements, company disclosures, operating data, industry context, and relevant macro indicators. Record sources, dates, units, and conflicts. For derivative analysis, also verify contract specifications and live/delayed market-data timestamps.

### 3. Underlying-asset analysis

For a company: examine its business model, industry position, value chain, profitability, cash flow, leverage, capital allocation, and relevant operational drivers. For an index: examine composition, concentration, sector drivers, earnings expectations, and market regime.

### 4. Valuation and scenario modelling

Where appropriate, estimate an **assumption-dependent range**, not a single unquestionable fair value. Compare market price, historical context, base/bull/bear cases, and sensitivity to major drivers. If data cannot support a credible valuation, say so.

### 5. Exposure and downside analysis

Connect the underlying thesis to a proposed contract or strategy. Examine expiry, strike, premium, implied volatility, Greeks, margin, liquidity, transaction costs, and scenario P&L. Distinguish the risk of being wrong about the asset from the risk of choosing an unsuitable instrument.

### 6. Decision memo and review

Produce an evidence-backed note with **thesis, supporting facts, assumptions, valuation/scenario range, downside, open questions, and a conditional conclusion**: investigate further, reject, or consider subject to human review. Retain a record of why the conclusion was reached.

## Example

Suppose a stock has rallied sharply and its call options appear attractive. The underwriting questions are not simply “Will it go higher?” or “Is the option cheap?”

- Has the underlying business improved, or has the market price moved faster than the fundamentals?
- What do earnings, margins, cash flow, operating performance, and valuation imply?
- What upcoming events could change the thesis before the option expires?
- How much of the option premium reflects volatility and time value?
- Under plausible downside and volatility scenarios, what happens to the proposed position?
- Is there enough evidence to proceed—or should the idea be rejected?

**Proposed output:** an auditable research memo, not a guaranteed prediction or an automatic buy/sell order.

## What problem is being solved?

**Asset price is an observation; asset quality and thesis strength require investigation.** A contract may be liquid and attractively priced relative to a model yet still express a weak or poorly understood view about the underlying.

The core failure mode to investigate is **taking exposure without a sufficiently documented thesis**: treating market moves as explanations, relying on stale figures, ignoring material events, or confusing a fundamental valuation with a short-term options payoff.

This project separates three questions:

1. **Asset:** What is the underlying and what fundamentally or economically drives its behavior?
2. **Thesis:** What evidence supports an expected scenario; what contradicts it; how sensitive is it to assumptions?
3. **Instrument fit:** If a derivative is being considered, is its horizon and risk profile consistent with that thesis?

The third question intersects with F&O Analyst, but **contract pricing, portfolio Greeks, and strategy selection principally belong there**. This engine should not duplicate the entire options workstation.

### Comparison with existing approaches

| Alternative | Strength | Research gap to test |
| --- | --- | --- |
| Price chart and market commentary | Fast view of market movements | Little evidence of underlying economic value or a falsifiable thesis |
| Equity research and company filings | Detailed fundamentals and context | Reconciling sources, assumptions and opposing evidence takes effort |
| Valuation spreadsheet | Quantified scenarios | Can hide source uncertainty and the decision narrative |
| Derivatives payoff calculator | Instrument-level mechanics | Does not establish why the underlying thesis should hold |

**First user:** me as a personal investment researcher. This is not a validated institutional underwriting workflow, a credit approval system, or an investment adviser.

## Outputs a reviewer should be able to audit

The target artifact is a compact **Underlying Asset & Thesis Assessment** with:

- Asset and market identification, scope, analysis date, and intended horizon.
- Evidence register: primary sources, periods, timestamps, unit conventions, and discrepancies.
- Driver map: company/industry factors for stocks; composition and economic/market drivers for indexes.
- Three-part thesis: evidence for it, evidence against it, and crucial unknowns.
- Conditional scenarios with major assumptions, plausible catalysts and invalidation conditions.
- Price versus estimated fundamental value or scenario range **when such a comparison is justified**.
- Confidence and data sufficiency assessment, without made-up probabilities.
- Decision state: *insufficient evidence / reject thesis / investigate further / conditional consideration*.
- Optional handoff notes to a separate derivatives risk review—not an order or a buy signal.

## Metrics: quality before automation

| Measure | Definition / test | Failure it helps detect |
| --- | --- | --- |
| Evidence traceability | Portion of key assertions linked to dated primary or clearly classified secondary sources | Unverifiable stories |
| Fact reconciliation | Material figures reproduced from published statements or official feeds | Incorrect units, periods or inputs |
| Thesis falsifiability | Portion of claims with a clear contradictory observation or invalidation test | Non-testable conviction |
| Risk coverage | Documented coverage of material financial, operational, macro, event and liquidity risks | Missing downside |
| Scenario reproducibility | Independent reviewer can recreate key scenarios using disclosed inputs | Hidden model judgment |
| Model sensitivity | How much the conclusion changes when the top uncertain assumptions are stressed | False precision |
| Time to reviewed memo | Analyst hours from scoped question to a signed-off research packet | Whether the workflow reduces groundwork |
| Guardrail breaches | Unsourced prices, undisclosed model assumptions, fabricated probabilities or automatic trades | Unacceptable errors |

These are **planned evaluation measures**, not measured performance. Do not quote an intrinsic-value estimate as an exchange-traded price or claim model correctness without a reference test.

### Potential research hypotheses

- A structured evidence register helps a reviewer find data conflicts earlier than an unstructured note.
- Separating **observed price**, **model-estimated value**, and **scenario payoff** reduces erroneous conclusions.
- Explicit contradicting evidence improves the discipline of a thesis decision.
- A standardized handoff to F&O Analyst (if ever built) reduces repeated context gathering without coupling the two products.

Each hypothesis should be tested against a simple manual memo before investing in an AI agent.

## Clear boundaries and project relationship

This is **capital-markets research focused on underwriting an underlying asset or investment thesis**. It is closest to **F&O Analyst**, which handles contracts, payoff, portfolio exposure and strategy-risk mechanics. They may exchange a human-reviewed research memo in the future; there is **no current software integration or mandatory sequence**.

**Project Matrix is a separate business diagnosis / turnaround / value-creation initiative.** It is not a component of this engine and should not appear in a live product pipeline. Its company research might become useful background someday, but that is explicitly **out of scope now**.

**API Intelligence** is an optional, independent concept for discovering, assessing and documenting reliable data sources. It is not a required operational dependency.

## First practical milestone

Choose **one underlying stock or index and one hypothetical derivative idea**. Assemble a source register, write an explicit thesis, perform a basic asset/market assessment, calculate at least three scenarios, and produce a one-page decision memo with a documented rejection criterion. Use historical or delayed data and independently check the calculations before adding automation.

**Potential measures:** source traceability, valuation/scenario reproducibility, coverage of material risks, clarity of assumptions, and consistency of decisions. No measured improvement or successful trade is claimed.

## Boundaries and unresolved decisions

- This is **research and decision support**, not regulated lending or insurance underwriting and not a personalized investment-advice service.
- The first scope is underlying-asset due diligence; it may later be separated from contract-level risk analysis if the overlap with F&O Analyst becomes too large.
- Financial valuation is inherently uncertain; a market price, intrinsic-value estimate, and derivative theoretical price are different things.
- The tool must not invent financial figures, contract quotes, or probabilities.
- No live trading, broker execution, autonomous capital allocation, or automatic approval is proposed.
- Data licensing, confidentiality, and explicit human review are required before any real-world use.

## Project documents

| Document | Purpose |
| --- | --- |
| [Original concept](docs/concept.md) | Earlier concept and assumptions; may reflect a different underwriting domain |
| [Proposed architecture](docs/architecture.md) | Earlier technical design, to be reconciled with this direction |
| [Development roadmap](docs/roadmap.md) | Earlier milestones, to be revised after scope validation |

These documents predate this clarified direction. The README is the current working thesis; detailed implementation choices remain open.
