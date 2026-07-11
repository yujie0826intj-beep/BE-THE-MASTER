# B_CONFIRM_CARD

TASK_ID:
FROM: B-V06 / btm-b-topic-gate
TO: D-V06 or Z
STATUS: DRAFT

## INPUT_CHECK

- Original B_TOPIC_DECISION_CARD is `GO`: yes/no
- S_THICK_DESCRIPTION_CARD gate passed: yes/no
- C_EVIDENCE_PACK present: yes/no
- C sufficiency result reviewed: yes/no

## C_EVIDENCE_REVIEW

- Evidence that supports the original thesis:
- Evidence that weakens or falsifies it:
- Unresolved source or data gaps:

## FINAL_QUESTION

-

## AUTHOR_THESIS_BOUNDARY

- Confirmed thesis:
- Claims that remain uncertain:
- Claims that are prohibited:

## EVIDENCE_BOUNDARY

- Evidence D/E may use:
- Evidence D/E must treat cautiously:
- Missing evidence D/E must not invent:

## CONFIRM_DECISION

Choose exactly one:

- `CONFIRM_GO_TO_D`
- `PIVOT_BEFORE_D`
- `RETURN_TO_C`
- `KILL`

## D_ENTRY_ALLOWED

- `YES` / `NO`

## D_STYLE_ROUTE_BRIEF

- Reader tension D must preserve:
- Counterevidence D must preserve:
- Causal boundaries D must preserve:

## PROCESS_PRODUCT_NOTE

B confirmation is an upstream process gate. It is never `PRODUCT_PASS`.
