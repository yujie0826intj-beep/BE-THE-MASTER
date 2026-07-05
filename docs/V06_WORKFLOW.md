# V06_WORKFLOW

## Fixed Route

```text
Z -> A -> S -> B -> C -> B_CONFIRM -> D -> E_MICRO_SAMPLE -> E_CONTROLLED_DRAFT -> F -> Z
```

## Stages

1. `Z_INIT`
   - Confirm task, material boundary, output path, and noise risk.
   - Create the round folder and dispatch package when the user explicitly starts a task.

2. `A_SOURCE`
   - Search or organize only the allowed material scope.
   - Output `A_SOURCE_PACKET.md`.
   - Separate facts, opinions, user feedback, and unverified claims.

3. `S_SIGNAL_ANALYSIS`
   - Turn A's materials into abnormal-signal and significance analysis.
   - Output `S_THICK_DESCRIPTION_CARD.md`.
   - Pass `S_STRUCTURAL_JUDGMENT_GATE`: macro/policy/industry or business-model frame, normal expectation, abnormal divergence, independent signals, mechanism, falsifier, and causal boundaries.
   - Form one reporter-style judgment candidate only if the structural gate passes; otherwise return to A/Z.
   - Do not write headlines, article structures, or draft language.

4. `B_TOPIC_GATE`
   - Decide whether the topic is worth writing.
   - Use S's thick description card as the judgment input.
   - Output `GO / PIVOT / KILL`.
   - Do not enrich evidence or write the draft.

5. `C_EVIDENCE`
   - Enrich evidence for B's topic decision.
   - Add data, cases, counterevidence, source ledger, timeline, and uncertainty boundaries.
   - Output `SUFFICIENT / INSUFFICIENT / ESCALATE`.

6. `B_CONFIRM`
   - Reconfirm the topic after C.
   - If evidence does not support the original angle, choose `PIVOT` or `KILL`.

7. `D_STYLE`
   - Select or propose a style card from `resources/style_cards/`.
   - Translate B/C boundaries into expression constraints.
   - Do not review the final draft.

8. `E_DRAFT`
   - Draft only from B/C/D handoffs.
   - Do not add facts, author judgments, or style routes.
   - For new angles, new style routes, or any route after human dissatisfaction, first output `E_MICRO_SAMPLE`.
   - Z must approve the micro sample before `E_CONTROLLED_DRAFT`.
   - Each round allows at most one rewrite.

9. `F_PRODUCT_REVIEW`
   - Output both `PROCESS_PASS/FAIL` and `PRODUCT_PASS/FAIL`.
   - Return the work to the correct upstream role when it fails.

10. `Z_CLOSE`
   - Record final status, attribution, reusable rules, and whether the topic continues.

## Routing Rules

- S `RETURN_TO_A_FOR_SOURCE_GAP`: return to A; do not continue to B.
- S `RETURN_TO_Z_FOR_HUMAN_JUDGMENT`: stop for Z/user judgment; do not continue to B.
- S `RETURN_TO_Z_FOR_SCOPE`: stop for Z/user scope decision.
- S `KILL_SIGNAL`: close the signal unless the user changes material scope.
- S `JUDGMENT_READY_FOR_B`: continue to B.
- B `KILL`: close the topic.
- B `PIVOT`: redefine the topic before continuing.
- C `INSUFFICIENT`: return to B; do not continue to D/E.
- D `STYLE_ROUTE_MISSING`: create or approve a style-card route before E.
- E fails once: allow one controlled rewrite only if the failure is expression execution.
- E fails twice: return to B/C/D; do not keep rewriting.
- F `PROCESS_PASS / PRODUCT_FAIL`: return to the responsible upstream role; do not assume another E rewrite.
- Human rejection after F `PRODUCT_PASS`: do not loop D/E/F by default; route by cause to S/B/C/D, and allow E only for a clear execution-only fix.

## Locked Baseline

Use `docs/V06_LOCKED_GENERATION_CHAIN.md` as the current minimum production baseline.

Future drafts must not be safer but weaker than `BTM-V06-FINAL-001`.
