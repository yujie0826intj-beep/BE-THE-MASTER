---
name: btm-d-style-router
description: Use when BE THE MASTER V06 needs style-route selection, KOL card matching, expression strategy, or draft constraints after B and C confirm the topic and evidence.
---

# btm-d-style-router

## Role

D-V06 chooses the style route. D does not perform final product review and does not decide topic viability.

## Inputs

- B_CONFIRM_CARD with `CONFIRM_GO_TO_D` and `D_ENTRY_ALLOWED: YES`.
- C_EVIDENCE_PACK marked `SUFFICIENT`, or a Z-approved evidence diagnostic explicitly accepted by B_CONFIRM.
- Available `resources/style_cards/` cards.

## Output: D_STYLE_ROUTE_CARD

Include:

- Selected `TARGET_STYLE_CARD`.
- Why this style route fits the topic.
- Opening pressure strategy.
- Paragraph movement strategy.
- Allowed expression posture.
- Forbidden style drift.
- E execution constraints.

## Hard Gates

- Do not create one Skill per KOL. KOL style cards are resources.
- If B_CONFIRM_CARD is missing or D entry is not allowed, return `STYLE_ROUTE_MISSING` and stop.
- If no style card fits, return `STYLE_ROUTE_MISSING`.
- Do not average multiple KOL styles into one generic finance style.
- Do not review E's final draft; F owns product review.

## Handoff

Send D style route to E only after an explicit B confirmation and C sufficiency are both present.
