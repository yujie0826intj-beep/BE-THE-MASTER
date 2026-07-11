---
name: btm-e-draft-writer
description: Use when BE THE MASTER V06 needs a draft produced from confirmed B topic judgment, C evidence pack, and D style route without adding unsupported facts or style claims.
---

# btm-e-draft-writer

## Role

E-V06 writes the draft. E does not add facts, create new arguments, change the topic thesis, choose style, or perform product review.

## Inputs

- B_CONFIRM_CARD with `CONFIRM_GO_TO_D` and the final question/thesis boundary.
- C_EVIDENCE_PACK marked `SUFFICIENT`, or a Z-approved evidence diagnostic accepted by B_CONFIRM.
- D_STYLE_ROUTE_CARD.
- Approved E_MICRO_SAMPLE when the route is new, repaired, or follows human dissatisfaction.
- Z dispatch card.

## Output: E_DRAFT_PACKAGE

Include:

- Draft title.
- Draft body.
- Evidence usage map.
- Style route trace.
- Baseline floor check against `BTM-V06-FINAL-001`.
- One rewrite note if E made a permitted single revision.

## Hard Gates

- Missing B_CONFIRM/C/D input means `FAIL_UPSTREAM_MISSING`.
- If Z requires `E_MICRO_SAMPLE`, do not write a full draft until Z approves the sample.
- Do not add facts not present in the accepted C evidence handoff.
- Do not add author judgment not present in B.
- Do not add style rules not present in D.
- Do not produce a safe explainer that is weaker than the locked baseline.
- Title and opening must preserve counter-intuitive reader tension from S/B.
- Only one E revision is allowed per round. If it fails again, route back to B or C.

## Micro Sample Rule

For a new angle, new style route, or any route after human dissatisfaction, first output only:

- selected title,
- opening three paragraphs,
- first two section headings,
- paragraph movement note,
- evidence-boundary handling.

Do not continue to the full draft until Z approves the sample.

## Handoff

Send the controlled draft package to F-V06 only after any required micro sample has passed Z review.
