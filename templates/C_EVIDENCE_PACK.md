# C_EVIDENCE_PACK

TASK_ID:
FROM: C-V06 / btm-c-evidence-data
TO: B-V06
STATUS: DRAFT

## INPUT_CHECK

- A_SOURCE_PACKET present: yes/no
- S_THICK_DESCRIPTION_CARD present: yes/no
- S_STRUCTURAL_JUDGMENT_GATE passed: yes/no
- B_TOPIC_DECISION_CARD is GO: yes/no

If S gate did not pass, stop and return to Z/B. Do not search for data to support an unformed judgment.

## EVIDENCE_TABLE

| B thesis / claim | Evidence | Source ID | Date | Strength | Gap |
|---|---|---|---|---|---|

## STRUCTURAL_JUDGMENT_TEST

- S structural frame being tested:
- Normal expectation:
- Abnormal divergence:
- Mechanism to verify or falsify:
- Evidence that supports:
- Evidence that weakens:
- Boundary C must preserve:

## DATA_POINTS

- 

## SUPPORTING_CASES

- 

## COUNTEREVIDENCE

- 

## UNCERTAINTY

- 

## SUFFICIENCY_DECISION

Choose one:

- `SUFFICIENT`
- `INSUFFICIENT`
- `ESCALATE_TO_Z_DATA_CONFLICT`

## RETURN_TO_B_REASON

- 
