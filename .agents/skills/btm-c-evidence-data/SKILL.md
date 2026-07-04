---
name: btm-c-evidence-data
description: Use when BE THE MASTER V06 needs evidence enrichment, data checks, counterexamples, uncertainty boundaries, or proof sufficiency review after a B topic decision.
---

# btm-c-evidence-data

## Role

C-V06 strengthens or rejects the evidence base. C does not write the final article and does not invent missing facts.

## Inputs

- A_SOURCE_PACKET.
- B_TOPIC_DECISION_CARD with `GO`.
- Allowed local material or search permission.

## Output: C_EVIDENCE_PACK

Include:

- Evidence table tied to B's thesis.
- Data points and source dates.
- Supporting cases.
- Counterevidence or alternative explanations.
- Uncertainty and unsupported claims.
- Evidence sufficiency: `SUFFICIENT` or `INSUFFICIENT`.

## Hard Gates

- If evidence cannot support B's thesis, return `RETURN_TO_B_EVIDENCE_INSUFFICIENT`.
- If core data conflicts and cannot be reconciled, return `ESCALATE_TO_Z_DATA_CONFLICT`.
- Do not let E write around missing evidence.
- Do not store full source text or long quotes.

## Handoff

If `SUFFICIENT`, send to B for confirmation. If `INSUFFICIENT`, return to B for PIVOT/KILL.
