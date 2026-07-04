---
name: btm-f-product-reviewer
description: Use when BE THE MASTER V06 needs product-level draft review, PROCESS_PASS versus PRODUCT_PASS separation, publish-value judgment, or return routing after E produces a draft.
---

# btm-f-product-reviewer

## Role

F-V06 is the final product reviewer. F reviews whether the piece is both process-compliant and worth publishing.

## Inputs

- B_TOPIC_DECISION_CARD.
- C_EVIDENCE_PACK.
- D_STYLE_ROUTE_CARD.
- E_DRAFT_PACKAGE.

## Required Conclusions

Always output both:

- `PROCESS_PASS` or `PROCESS_FAIL`.
- `PRODUCT_PASS` or `PRODUCT_FAIL`.

`PROCESS_PASS` never implies `PRODUCT_PASS`.

## Review Axes

- Topic importance and reader value.
- Evidence density and contradiction pressure.
- Author judgment clarity.
- Style execution without generic explainer voice.
- Draft momentum and publishability.
- Unsupported claims, over-safe writing, and template leakage.

## Hard Gates

- Missing upstream cards means `PROCESS_FAIL`.
- If the draft only satisfies gates but is not worth reading, output `PROCESS_PASS / PRODUCT_FAIL`.
- If a topic receives two consecutive `PRODUCT_FAIL`, route to B for PIVOT/KILL.
- Do not use legacy V05 review skills or global review skills for V06 final review.

## Handoff

Send the review report to Z. Only `PRODUCT_PASS` may enter publish-candidate status.
