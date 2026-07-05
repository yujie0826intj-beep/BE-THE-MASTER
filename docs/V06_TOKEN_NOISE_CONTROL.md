# V06_TOKEN_NOISE_CONTROL

## Goal

Spend tokens on topic judgment, evidence, style route, and product quality. Avoid screen spam, old-thread rehydration, and endless rewrites.

## Freeze Rules

1. Do not start heartbeat automation.
2. Do not continue V05/R6 micro-fixes.
3. Do not read long old-thread context.
4. Historical failures should come from local private records or public-safe summaries, not full old thread bodies.
5. Each patrol or check may perform at most one state-changing action.

## Locked Input Priority

When later roles receive overlapping cards or pasted context, use this priority:

1. `Z_FINAL_ROUND_REVIEW`
2. `F_PRODUCT_REVIEW_REPORT`
3. `E_CONTROLLED_DRAFT`
4. `E_MICRO_SAMPLE`
5. `D_STYLE_ROUTE_CARD`
6. `B_CONFIRM_CARD`
7. C evidence pack or diagnostic pack
8. `B_TOPIC_DECISION_CARD`
9. `S_THICK_DESCRIPTION_CARD`
10. `A_SOURCE_PACKET`

Earlier dispatch text, partial role outputs, or chat-order artifacts are historical process noise unless Z explicitly promotes them.

Pre-S production attempts are noise by default for future production. Use them only as failure examples or diagnostics.

## Low-Noise Execution

- Pure status checks should not notify unless blocked or user action is needed.
- Do not revive old threads.
- Do not write to the legacy root.
- E may rewrite once per round at most.
- E must use a micro sample before full drafting when the route is new or follows human dissatisfaction.
- F review should be short and decisive: product decision first, explanation second.

## High-Noise Signals

- The same role repeatedly rereads the full rule set.
- Multiple rounds only adjust forbidden words without revisiting topic or evidence.
- D/F produce long reviews without product conclusions.
- Z keeps adding gates without stopping the route.
- A role tries to fill another role's missing output.
- A later role reads pre-S drafts as positive examples.
- E writes a full draft without a passed micro sample on a new or repaired route.

## Z Handling

When high-noise signals appear, Z must stop dispatch and offer the user 2-3 business choices.
