---
name: btm-b-topic-gate
description: Use when BE THE MASTER V06 needs topic viability judgment, expectation-gap analysis, author thesis validation, or GO/PIVOT/KILL decisions before evidence enrichment.
---

# btm-b-topic-gate

## Role

B-V06 has topic life-or-death authority. B decides whether the topic can support a deep publishable article.

## Inputs

- Z dispatch card.
- A_SOURCE_PACKET.
- S_THICK_DESCRIPTION_CARD.
- Any prior user constraints.

## Output: B_TOPIC_DECISION_CARD

Always output exactly one decision:

- `GO`: topic has reader tension, evidence path, and author judgment.
- `PIVOT`: topic is promising but needs a narrower angle or different question.
- `KILL`: topic is not worth writing with current material.

Also include:

- Why this topic matters now.
- The expectation gap.
- Core author thesis.
- Whether S passed `S_STRUCTURAL_JUDGMENT_GATE`.
- Whether S's judgment bridge is strong enough or should be narrowed.
- Required evidence to prove or challenge the thesis.
- Reader value.
- Risk of generic explainer writing.

## Hard Gates

- If A packet lacks source/date/number basics, return `RETURN_TO_A_SOURCE_GAP`.
- If S card is missing, one-sentence judgment is absent, or the abnormal signal is not explained, return `RETURN_TO_S_JUDGMENT_GAP`.
- If S did not pass `S_STRUCTURAL_JUDGMENT_GATE`, return `RETURN_TO_S_JUDGMENT_GAP` or `RETURN_TO_A_SOURCE_GAP`; do not rescue S by inventing the macro/policy/industry frame yourself.
- If S's judgment depends on one isolated fact, user wording, a single news item, or an unverified opinion, return `RETURN_TO_A_SOURCE_GAP`.
- If S has no falsifier or no causal boundary, return `RETURN_TO_S_JUDGMENT_GAP`.
- If the topic only supports a safe explainer, return `KILL`.
- If evidence may support another angle better, return `PIVOT`.
- If C later finds evidence insufficient, B must re-confirm GO/PIVOT/KILL.

## Handoff

Only `GO` goes to C-V06. `PIVOT` and `KILL` return to Z.
