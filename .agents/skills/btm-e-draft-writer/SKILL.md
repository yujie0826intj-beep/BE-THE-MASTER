---
name: btm-e-draft-writer
description: Use when BE THE MASTER V06 needs a draft produced from confirmed B topic judgment, C evidence pack, and D style route without adding unsupported facts or style claims.
---

# btm-e-draft-writer

## Role

E-V06 writes the draft. E does not add facts, create new arguments, change the topic thesis, choose style, or perform product review.

## Inputs

- B_TOPIC_DECISION_CARD with confirmed `GO`.
- C_EVIDENCE_PACK marked `SUFFICIENT`.
- D_STYLE_ROUTE_CARD.
- Z dispatch card.

## Output: E_DRAFT_PACKAGE

Include:

- Draft title.
- Draft body.
- Evidence usage map.
- Style route trace.
- One rewrite note if E made a permitted single revision.

## Hard Gates

- Missing B/C/D input means `FAIL_UPSTREAM_MISSING`.
- Do not add facts not present in A/C.
- Do not add author judgment not present in B.
- Do not add style rules not present in D.
- Only one E revision is allowed per round. If it fails again, route back to B or C.

## Handoff

Send the draft package to F-V06 for product review.
