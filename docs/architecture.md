# Underwriting Engine — Proposed Architecture

**Status:** Exploratory sketch. No components are implemented or validated yet.

```text
Application intake
   ↓
Validation
   ↓
Rules/assessment
   ↓
Review
   ↓
Audit record
```

## Components and responsibilities

| Component | Proposed role |
| --- | --- |
| Application intake | Domain-specific application and required evidence (TBD) |
| Validation | Check completeness, provenance and consistency of inputs |
| Rules/assessment | Versioned decision policy to be explicitly designed and reviewed |
| Review | Human-in-the-loop exceptions, overrides and rationale |
| Audit record | Inputs used, policy version, decision state, supporting explanation |

## Design principles

- Make every assumption visible and revisit it after real user discovery.
- Keep deterministic calculations and policy checks distinct from AI-generated explanations.
- Track data provenance, timestamps, source limitations and confidence as applicable.
- Prefer minimal dependencies and local/synthetic tests before live integrations.
- Do not store secrets in code or repository files.

## Decisions still open

- What type of underwriting: loans, insurance, merchant, investment or another domain?
- Who has authority to approve/decline, and is the system advisory or decisional?
- Which jurisdiction and regulations apply?
- What information is legally and ethically permitted to inform decisions?
