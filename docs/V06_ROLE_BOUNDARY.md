# V06_ROLE_BOUNDARY

## Boundary Principle

Each role has one main job. If upstream material is missing, the role must `FAIL` or `ESCALATE`; it must not fill the missing work itself.

## Role Boundary Table

| Role | Can Do | Must Not Do |
|---|---|---|
| Z | Orchestrate, register, attribute issues, approve reusable rules | Write drafts, review drafts, replace another role's output |
| A | Scout sources, label sources, split fact/opinion, mark source risks | Decide whether the topic is worth writing, choose style, write drafts |
| S | Interpret abnormal signals, pass `S_STRUCTURAL_JUDGMENT_GATE`, explain why they matter, form one reporter-style judgment candidate, write the thick description card | Write drafts, choose style, enrich evidence broadly, decide final topic life-or-death, form judgments from thin A material |
| B | Judge topic, find expectation gap, validate S's judgment, output `GO/PIVOT/KILL` | Invent a missing core judgment, enrich evidence, write the draft, review the final article |
| C | Enrich evidence, check data, find counterevidence, judge evidence sufficiency | Force writing, change B's thesis, choose style, search for data to support a failed or thin S judgment |
| D | Choose style route, style card, expression strategy, draft constraints | Review final product, change facts, change thesis |
| E | Draft micro sample and controlled full draft from B/C/D only | Add facts, judgments, style routes, or skip required micro sample |
| F | Product review and return routing | Replace D with old review skills or rewrite the article |

## Thread Rules

- Each role may have at most one active V06 thread.
- If no V06 thread exists for a role, its status is `idle/unassigned`.
- Old A/B/C/D threads must be archived and are not dispatch targets.
- Real thread IDs stay in `local_registry/`, not public `registry/`.

## Handoff Rules

- A hands source boundaries to S.
- S hands a thick description and judgment candidate to B.
- B hands a topic decision to C.
- C hands evidence sufficiency back to B.
- B confirms the final question before D.
- D hands a style route to E.
- E hands a micro sample to Z when required.
- Z approves the micro sample before E writes the controlled full draft.
- E hands a controlled draft package to F.
- F hands product judgment and return route to Z.
