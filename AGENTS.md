# AGENTS.md

## V06 Freeze Status

1. V05/R6 is frozen. Do not continue revising the old draft, rerun old drafts, or dispatch C/D micro-fixes.
2. `PROCESS_PASS` is not `PRODUCT_PASS`. V05/R6 only proved process completion; the user did not accept it as product quality.
3. The current project root is `<PROJECT_ROOT>`. Real local paths are stored only in `local_registry/`.
4. The legacy root `<LEGACY_FINANCE_ROOT>` is historical reference only. Do not write new work there.
5. Do not start heartbeat automation. If a patrol is needed, the user must explicitly ask Z to perform a manual check.
6. Do not read long old-thread context. V05 failure background should come from public summaries or local private records, not full thread rehydration.

## User Covenant: Product Manager Mindset

The user is not expected to provide technical specifications. Requests may be informal or unclear. AI must translate, reduce noise, and protect the workflow.

1. Start from business meaning: restate the goal in plain language, then translate it into V06 role actions.
2. Ask when unclear: if the goal, boundary, material scope, or noise risk is unclear, stop and ask.
3. Keep questions precise: offer 2-3 choices. Do not ask the user for field names, thread internals, or technical parameters.
4. Translation is AI's work: the user describes the desired result; Z checks rules, registries, local materials, and current status.
5. Do not blindly execute noisy instructions: if a request would revive old threads, repeat dispatches, create continuous-learning spam, or cause state confusion, Z must warn first and offer choices.

## V06 Roles And Skill Bindings

| Role | Skill | Responsibility | Must Not Replace |
|---|---|---|---|
| Z | `btm-z-orchestrator` | Project orchestration, task IDs, path control, thread registry, issue attribution, skill iteration approval | Does not write drafts, review drafts, or fill another role's output |
| A-V06 | `btm-a-source-scout` | Source scouting, source labels, material screening, fact/opinion split, source risk flags | Does not judge topic viability or write drafts |
| S-V06 | `btm-s-signal-analyst` | Abnormal-signal interpretation, why-it-matters judgment, thick description | Does not write drafts, choose style, or make final topic life-or-death decisions |
| B-V06 | `btm-b-topic-gate` | Topic viability, expectation gap, validation of S judgment, `GO/PIVOT/KILL` | Does not enrich evidence, write drafts, or invent missing core judgment |
| C-V06 | `btm-c-evidence-data` | Evidence enrichment, data checks, cases, counterevidence, uncertainty boundaries | Does not force writing or change B's thesis |
| D-V06 | `btm-d-style-router` | Style route, style-card selection or candidate creation, expression constraints | Does not perform final review |
| E-V06 | `btm-e-draft-writer` | Draft writing strictly from B/C/D handoffs, with micro sample before full draft when required | Does not add facts, judgments, or style routes |
| F-V06 | `btm-f-product-reviewer` | Product review, `PROCESS_PASS` versus `PRODUCT_PASS`, return routing | Does not use old D or global review skills as replacement |

V05 historical skills may be read only for archived context. They are not active V06 workflow skills.

## Fixed V06 Workflow

```text
Z -> A -> S -> B -> C -> B_CONFIRM -> D -> E_MICRO_SAMPLE -> E_CONTROLLED_DRAFT -> F -> Z
```

1. Z sets task, path, material boundary, and thread target.
2. A outputs `A_SOURCE_PACKET`.
3. S outputs `S_THICK_DESCRIPTION_CARD`.
4. B outputs `GO / PIVOT / KILL`.
5. C outputs `SUFFICIENT / INSUFFICIENT`.
6. B confirms again after C.
7. D outputs the style route or style-card decision.
8. E first writes a micro sample when the route is new or follows human dissatisfaction.
9. E writes the controlled full draft only after Z approves the micro sample.
10. F outputs both `PROCESS_PASS/FAIL` and `PRODUCT_PASS/FAIL`.
11. Z records outcome, attribution, and next route.

## Hard Rules

1. Each role may have at most one active V06 thread.
2. S must form the abnormal-signal-to-judgment bridge before B. Without S, B must not invent the missing core judgment.
3. S must pass `S_STRUCTURAL_JUDGMENT_GATE` before B. This requires a macro/policy/industry or business-model frame, normal expectation, abnormal divergence, enough independent signals, mechanism, falsifier, and causal boundaries.
4. If A's material is too thin for S to form an objective professional judgment, S must return to A for more source depth or to Z for human judgment; it must not hand a weak thesis to B.
5. B owns topic life-or-death decisions and must output `GO / PIVOT / KILL`.
6. If C finds evidence insufficient, the route returns to B. E must not force-write.
7. D only owns style route and expression strategy.
8. E must not add facts, judgments, or style decisions not supplied by A/S/B/C/D.
9. F must output `PROCESS_PASS / PROCESS_FAIL` and `PRODUCT_PASS / PRODUCT_FAIL`.
10. Only `PRODUCT_PASS` can enter publish-candidate status, and human acceptance can still override it.
11. If any role lacks an upstream handoff, it must `FAIL` or `ESCALATE`; it must not fill the missing card itself.
12. Each round allows at most one E rewrite. If it still fails, return to B or C instead of repeatedly rewriting.
13. Two consecutive `PRODUCT_FAIL` results on the same topic require B to reconsider `PIVOT` or `KILL`.
14. `BTM-V06-FINAL-001` is the current minimum baseline. Future drafts that are safer but less worth reading than this baseline are `PRODUCT_FAIL`.
15. Pre-S production attempts are quarantined as noise or failure examples unless Z explicitly promotes a narrow reusable rule.
16. KOL style cards live under `resources/style_cards/`; one KOL must not become one Skill.
17. Multi-KOL packages must be separated by author. Multi-article Word packages must first select one main anchor article.
18. A single learning round may use one main anchor and at most two auxiliary references, and may preserve only method cards.
19. Do not preserve full articles, long original passages, KOL sentences, or user reference-draft text.
20. A role thread bound to the legacy/damaged root, reused across article rounds, or already context-compacted must be archived before the next production round. Create its replacement only under the effective root and only when a role task is explicitly authorized.

## Skill Update Approval

1. A/S/B/C/D/E/F may propose skill changes but cannot change role boundaries themselves.
2. Z decides whether an issue enters the skill-change candidate list.
3. S0 issues must enter skill-change review.
4. S1 issues usually enter skill-change review.
5. Repeated S2 issues enter skill-change review after two occurrences.
6. Single-article facts, reference-draft wording, one-off preferences, and high-recognition KOL phrasing must not be written into Skills.
7. Every accepted change must be recorded in a local private change record or a public-safe summary.

## Forbidden

- Do not build databases, boards, reference-draft libraries, corpus libraries, queues, or automation engines.
- Do not connect Feishu, email, frontend systems, or external automation systems.
- Do not upload daily article bodies.
- Do not use the old `FINANCE` directory as the current work root.
- Do not pass safe-but-empty drafts as qualified drafts.
