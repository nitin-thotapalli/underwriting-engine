# Underwriting Engine — Original Concept & Scope

> **Current direction (superseding the generic proposal below):** The original note said only “Underwriting engine,” so the earlier credit/insurance application workflow was a speculative interpretation. The [README](../README.md) now defines **investment/underlying-asset thesis assessment for personal capital-markets research**, most closely related to F&O Analyst. Loan approval, insurance eligibility and applicant scoring are **not in scope**. The original brainstorm below is preserved as historical context, not as the current product requirement.

## Original idea (from Notion)

> Underwriting engine

The source note is a title only. The purpose, underwriting domain, intended user, eligibility rules, data sources and operating constraints have **not** been specified. Everything below is an initial exploration proposal—not an approved product specification.

## Problem hypothesis

Potentially support an underwriter in reviewing an application, checking evidence, applying defined criteria and documenting an explainable decision. The concrete problem is not yet specified.

## Intended audience (hypothesis)

To be determined after choosing an underwriting domain (for example, credit, insurance or another risk assessment workflow).

## Scope to investigate

- Define underwriting domain, decision owner and intended use before designing rules.
- Describe application inputs, permitted source evidence and minimum documentation.
- Sketch an auditable decision workflow: intake → validation → policy checks → manual review → outcome.
- Record reasons, uncertainty, exceptions and human overrides.
- Use synthetic examples before handling any personal or regulated data.

## What this project does **not** yet provide

- A functioning credit, insurance or risk-scoring engine.
- Approval or rejection rules, thresholds, model coefficients or fairness claims.
- Integration with real applicant data, external bureaus, financial records or automated decision-making.

## Questions to resolve

- [ ] What type of underwriting: loans, insurance, merchant, investment or another domain?
- [ ] Who has authority to approve/decline, and is the system advisory or decisional?
- [ ] Which jurisdiction and regulations apply?
- [ ] What information is legally and ethically permitted to inform decisions?

## Source and provenance

