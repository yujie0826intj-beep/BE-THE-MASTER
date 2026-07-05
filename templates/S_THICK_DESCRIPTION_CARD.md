# S_THICK_DESCRIPTION_CARD

TASK_ID:
FROM: S-V06 / btm-s-signal-analyst
TO: B-V06 or Z
STATUS: DRAFT

## INPUT_CHECK

- A_SOURCE_PACKET present: yes/no
- Allowed material scope clear: yes/no
- Abnormal signal present: yes/no
- Source/date/number basics enough for judgment formation: yes/no
- Macro/policy/industry/business-model frame present: yes/no
- At least two independent signal categories present: yes/no

## S_STRUCTURAL_JUDGMENT_GATE

Choose one:

- `PASS`
- `FAIL_RETURN_TO_A_FOR_SOURCE_GAP`
- `FAIL_RETURN_TO_Z_FOR_HUMAN_JUDGMENT`
- `FAIL_RETURN_TO_Z_FOR_SCOPE`
- `FAIL_KILL_SIGNAL`

Required checks:

| Check | Result | Notes |
|---|---|---|
| Macro/policy/industry/business-model frame exists | pass/fail | |
| Normal expectation is stated | pass/fail | |
| Abnormal divergence is stated | pass/fail | |
| Independent signal categories are sufficient | pass/fail | |
| Mechanism links signals to judgment | pass/fail | |
| Falsifier is stated | pass/fail | |
| Causal boundaries are stated | pass/fail | |

## ABNORMAL_SIGNAL

- What changed, diverged, contradicted expectations, or looked structurally unusual?

## WHY_IT_MATTERS_NOW

- Why should a reader care now?
- What public/common-sense reading is insufficient?

## STRUCTURAL_CONTEXT

- Macro/policy/industry background:
- Normal expectation for this company/institution/sector:
- Abnormal divergence from that expectation:
- Company/institution incentives:
- Financial/data pattern:
- Regulatory or governance context:
- Business mechanism or constraint:
- Future choice narrowed:

## JUDGMENT_CANDIDATE

One sentence only:

-

## JUDGMENT_TYPE

Choose one or more:

- financial-statement signal
- policy/regulatory signal
- governance/control signal
- industry-cycle signal
- funding/liquidity signal
- contradiction between public data and event outcome
- other:

## EVIDENCE_PATH

| Judgment component | Evidence needed | Current evidence | Gap |
|---|---|---|---|

## COUNTEREVIDENCE_AND_FAILURE_CONDITIONS

| What could weaken or falsify the judgment | Current status |
|---|---|

## MATERIAL_THICKNESS

Choose one:

- `STRONG`
- `MEDIUM`
- `WEAK`
- `INSUFFICIENT`

Reason:

-

Independent signal categories counted:

- Category 1:
- Category 2:
- Category 3 if any:

## DECISION

Choose exactly one:

- `JUDGMENT_READY_FOR_B`
- `RETURN_TO_A_FOR_SOURCE_GAP`
- `RETURN_TO_Z_FOR_HUMAN_JUDGMENT`
- `RETURN_TO_Z_FOR_SCOPE`
- `KILL_SIGNAL`

## HANDOFF_TO_B

If ready for B:

- Core judgment to test:
- Expectation gap to test:
- Evidence path B must preserve:
- Boundaries B must not cross:

If not ready:

- Return target:
- Reason:
