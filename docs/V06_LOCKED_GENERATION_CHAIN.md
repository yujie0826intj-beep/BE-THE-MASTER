# V06_LOCKED_GENERATION_CHAIN

## Purpose

This file locks the first V06 chain that produced a user-recognized quality improvement after adding S-V06.

It does not preserve article text. It preserves the generation route, gates, quality floor, and noise cleanup rule.

## Locked Baseline

Baseline round: `BTM-V06-FINAL-001`

Publish-candidate source:

`local_working/rounds/BTM-V06-E-CONTROLLED-DRAFT-001/E/E_CONTROLLED_DRAFT.md`

F review:

`local_working/rounds/BTM-V06-F-REVIEW-001/F/F_PRODUCT_REVIEW_REPORT.md`

This baseline is not a perfect article. It is the minimum acceptable floor for the next production attempt.

## Minimum Quality Floor

Future drafts must be at least as strong as this baseline in the following ways:

1. The title and first three paragraphs must create a real reader question through counter-intuitive tension.
2. The article must start from a reporter judgment, not from a safe explainer structure.
3. The draft must preserve the S-to-B abnormal-signal judgment chain.
4. Evidence must show contradiction pressure, not just supporting facts.
5. Counterevidence must be inside the article, not only in review notes.
6. The draft must keep causal boundaries without becoming a boundary-only article.
7. F must judge reading value, not only compliance.

If a later draft is safer but less interesting than this baseline, it is `PRODUCT_FAIL`.

## Locked Route

Default production route:

```text
Z -> A -> S -> B -> C -> B_CONFIRM -> D -> E_MICRO_SAMPLE -> E_CONTROLLED_DRAFT -> F -> Z
```

## Required Artifacts

| Stage | Artifact | Hard requirement |
|---|---|---|
| A | `A_SOURCE_PACKET.md` | Source scope, fact/opinion split, risk flags |
| S | `S_THICK_DESCRIPTION_CARD.md` | Passed `S_STRUCTURAL_JUDGMENT_GATE` |
| B | `B_TOPIC_DECISION_CARD.md` | `GO/PIVOT/KILL`, preserves or rejects S judgment |
| C | evidence pack or diagnostic pack | Evidence, counterevidence, data gaps, source ledger |
| B_CONFIRM | `B_CONFIRM_CARD.md` | Final question, thesis boundary, D allowance |
| D | style route card | Specific style route and expression constraints |
| E micro | `E_MICRO_SAMPLE.md` | Title/opening/section rhythm tested before full draft |
| E controlled | `E_CONTROLLED_DRAFT.md` | Full draft only after micro sample passes |
| F | `F_PRODUCT_REVIEW_REPORT.md` | `PROCESS_PASS/FAIL` and `PRODUCT_PASS/FAIL` |
| Z | `Z_FINAL_ROUND_REVIEW.md` | Publish candidate or return route |

## Mandatory E Micro Sample Gate

E must not jump directly from D to full article when the task involves a new angle, new style route, or prior human dissatisfaction.

Before full drafting, E must produce a micro sample containing:

1. selected title,
2. opening three paragraphs,
3. first two section headings,
4. intended paragraph movement,
5. evidence-boundary handling.

Z must inspect the micro sample before allowing the full E draft.

If the micro sample lacks reader tension, F should not be needed; Z returns to D or B.

## No-S Noise Quarantine

Pre-S production attempts are not reusable route evidence.

They may be used only as:

1. failure examples,
2. noise diagnostics,
3. proof that source-to-topic jumping was insufficient.

They must not be used as direct drafting input for later E tasks.

Canonical post-S chain begins at `BTM-V06-SB-REPLAY-002`.

## Human Rejection Rule

If a human rejects a draft after F `PRODUCT_PASS`, do not automatically loop D/E/F.

Z must route the rejection by cause:

1. weak judgment or finance intuition: return to S learning or B;
2. missing evidence: return to C;
3. wrong angle: return to B;
4. wrong expression route: return to D;
5. execution-only issue: allow one E controlled rewrite.

