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
- Required evidence to prove or challenge the thesis.
- Reader value.
- Risk of generic explainer writing.

## Hard Gates

- If A packet lacks source/date/number basics, return `RETURN_TO_A_SOURCE_GAP`.
- If the topic only supports a safe explainer, return `KILL`.
- If evidence may support another angle better, return `PIVOT`.
- If C later finds evidence insufficient, B must re-confirm GO/PIVOT/KILL.

## Handoff

Only `GO` goes to C-V06. `PIVOT` and `KILL` return to Z.
