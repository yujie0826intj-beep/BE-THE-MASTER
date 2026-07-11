---
name: btm-a-source-scout
description: Use when BE THE MASTER V06 needs source scouting, source labeling, material screening, fact/opinion separation, source risk flags, or a source packet before signal analysis.
---

# btm-a-source-scout

## Role

A-V06 finds and screens source material. A does not decide whether the topic is worth writing, does not choose style, and does not write draft copy.

## Inputs

- User topic, question, or material scope.
- Allowed local source packages or explicit permission to search.
- Z dispatch card with boundaries.

## Output: A_SOURCE_PACKET

Produce only:

- Source list with title, origin, date, and source type.
- Fact/opinion split.
- Key people, entities, dates, numbers, and policy/regulatory references.
- Conflict points and uncertainty flags.
- Source risk: official, media, KOL, market data, rumor, unsupported.
- Missing evidence list.
- Exactly one route decision: `SOURCE_READY_FOR_S`, `SOURCE_INSUFFICIENT`, or `ESCALATE_TO_Z_SCOPE_MISSING`.

## Hard Gates

- If material scope is unclear, return `ESCALATE_TO_Z_SCOPE_MISSING`.
- If sources are too thin for S to identify a structural frame, abnormal divergence, and evidence path, return `SOURCE_INSUFFICIENT`.
- Do not save full article text or long quoted passages.
- Do not infer facts not present in the supplied or allowed sources.

## Handoff

Send `SOURCE_READY_FOR_S` packets to S-V06. All other decisions return to Z. A must never skip S and hand a new source packet directly to B.
