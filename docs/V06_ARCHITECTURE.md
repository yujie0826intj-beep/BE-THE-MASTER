# V06_ARCHITECTURE

## Goal

V06 does not continue patching V05/R6. It turns BE THE MASTER from a gate-loop system into a low-noise editorial chain:

```text
detect source signals -> form a reporter judgment -> judge the topic -> enrich evidence -> select style route -> micro sample -> controlled draft -> product review
```

## Fixed Roots

- Current root: `<PROJECT_ROOT>`
- Legacy root: `<LEGACY_FINANCE_ROOT>`
- Real local paths belong only in `local_registry/`.
- The legacy root is historical reference only. Do not write new work there.

## Role Structure

| Role | Name | Core responsibility | Output |
|---|---|---|---|
| Z | Orchestrator | Task ID, path control, registry, issue attribution, iteration approval | `Z_ROUND_REVIEW` |
| A-V06 | Source scout | Sources, source labels, fact/opinion split, risk flags | `A_SOURCE_PACKET` |
| S-V06 | Signal analyst | Abnormal signal interpretation, why-it-matters judgment, thick description | `S_THICK_DESCRIPTION_CARD` |
| B-V06 | Topic gate | Topic value, expectation gap, author thesis, `GO/PIVOT/KILL` | `B_TOPIC_DECISION_CARD` |
| C-V06 | Evidence and data | Data, cases, counterevidence, uncertainty boundaries | `C_EVIDENCE_PACK` |
| D-V06 | Style router | Style-card selection or candidate creation, expression strategy | `D_STYLE_ROUTE_CARD` |
| E-V06 | Draft writer | Micro sample and controlled draft strictly from B/C/D handoffs | `E_MICRO_SAMPLE`, `E_CONTROLLED_DRAFT` |
| F-V06 | Product reviewer | Product-level review, `PROCESS_PASS` versus `PRODUCT_PASS` | `F_PRODUCT_REVIEW_REPORT` |

## Key Changes From V05

1. S is added between A and B to form the reporter-style judgment candidate from abnormal signals.
2. B owns topic viability and can stop weak topics, but B should not invent the core judgment if S did not form one.
3. C returns evidence-insufficient cases to B instead of letting E force-write.
4. D is no longer a reviewer. D only owns style route and expression constraints.
5. F owns final product review.
6. `PROCESS_PASS` is not `PRODUCT_PASS`.
7. E must use a micro sample before full drafting when the route is new, repaired, or follows human dissatisfaction.
8. F compares future drafts against `BTM-V06-FINAL-001` as the current minimum baseline.
9. Each round allows at most one E rewrite.
10. Old A/B/C/D threads and pre-S production attempts are archived or quarantined and cannot become V06 dispatch targets.

## Asset Model

Reusable assets are stored as:

- style cards in `resources/style_cards/`
- handoff templates in `templates/`
- public-safe process rules in `docs/`
- private operational records in `local_registry/` and `local_working/`

Old learning output can be reused only after Z approves it as a V06 asset. Do not directly use old thread context or full articles.
