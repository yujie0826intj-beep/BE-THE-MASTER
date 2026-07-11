---
name: btm-f-product-reviewer
description: Use when BE THE MASTER V06 needs product-level draft review, PROCESS_PASS versus PRODUCT_PASS separation, publish-value judgment, or return routing after E produces a draft.
---

# btm-f-product-reviewer

## Role

F-V06 is the final product reviewer. F reviews whether the piece is both process-compliant and worth publishing.

## Inputs

- B_CONFIRM_CARD.
- C_EVIDENCE_PACK or a Z-approved compact evidence handoff.
- D_STYLE_ROUTE_CARD.
- E_MICRO_SAMPLE gate result when required.
- E_CONTROLLED_DRAFT package.

## Required Conclusions

Always output both:

- `PROCESS_PASS` or `PROCESS_FAIL`.
- `PRODUCT_PASS` or `PRODUCT_FAIL`.

`PROCESS_PASS` never implies `PRODUCT_PASS`.

## Review Axes

- Topic importance and reader value.
- Whether the draft preserves the abnormal-signal-to-judgment bridge recorded in B_CONFIRM.
- Evidence density and contradiction pressure.
- Author judgment clarity.
- Style execution without generic explainer voice.
- Draft momentum and publishability.
- Unsupported claims, over-safe writing, and template leakage.
- Whether the title and first three paragraphs are at least as strong as the locked baseline in `BTM-V06-FINAL-001`.

## Hard Gates

- Missing B_CONFIRM, C, D, E, or a required micro-sample gate means `PROCESS_FAIL`.
- If the draft is accurate but lacks a real reporter judgment, output `PROCESS_PASS / PRODUCT_FAIL` and attribute the failure to missing S/B judgment formation.
- If the draft only satisfies gates but is not worth reading, output `PROCESS_PASS / PRODUCT_FAIL`.
- If the draft is safer but less interesting than `BTM-V06-FINAL-001`, output `PROCESS_PASS / PRODUCT_FAIL`.
- If E skipped a required micro sample, output `PROCESS_FAIL`.
- If a topic receives two consecutive `PRODUCT_FAIL`, route to B for PIVOT/KILL.
- Do not use legacy V05 review skills or global review skills for V06 final review.
- Do not read full role-thread history. Prefer the latest locked handoffs and a compact C evidence pack.

## Baseline Floor

Compare every product review against `docs/V06_LOCKED_GENERATION_CHAIN.md`.

Minimum checks:

- counter-intuitive title/opening tension,
- clear abnormal-signal judgment,
- contradiction pressure from evidence,
- counterevidence inside the draft,
- causal boundaries without killing reading momentum.

Compliance is not enough. A draft below this floor is not a publish candidate.

## Handoff

Send the review report to Z. Only `PRODUCT_PASS` may enter publish-candidate status.
