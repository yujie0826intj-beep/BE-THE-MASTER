# BE THE MASTER

BE THE MASTER is a public architecture repository for a V06 editorial-agent workflow. It stores reusable rules, role boundaries, handoff templates, quality gates, and project-local Codex skills.

It does not store article drafts, raw news, private source packs, local thread IDs, local paths, screenshots, daily outputs, or unpublished copy.

## V06 Architecture

```text
Z -> A -> B -> C -> B_CONFIRM -> D -> E -> F -> Z
```

| Role | Responsibility | Skill |
|---|---|---|
| Z | Orchestration, path control, registry, issue attribution, skill approval | `btm-z-orchestrator` |
| A-V06 | Source scouting, source labeling, fact/opinion separation, risk flags | `btm-a-source-scout` |
| B-V06 | Topic viability, expectation gap, author thesis, GO/PIVOT/KILL | `btm-b-topic-gate` |
| C-V06 | Evidence enrichment, data checks, counterevidence, sufficiency | `btm-c-evidence-data` |
| D-V06 | Style routing and KOL style-card selection | `btm-d-style-router` |
| E-V06 | Draft writing from confirmed B/C/D inputs | `btm-e-draft-writer` |
| F-V06 | Product review, PROCESS_PASS vs PRODUCT_PASS | `btm-f-product-reviewer` |

## Core Rule

`PROCESS_PASS` is not `PRODUCT_PASS`.

Only `PRODUCT_PASS` may enter publish-candidate status.

## Repository Contents

```text
AGENTS.md
docs/
  V06_ARCHITECTURE.md
  V06_WORKFLOW.md
  V06_ROLE_BOUNDARY.md
  V06_QUALITY_GATES.md
  V06_PRODUCT_PASS_STANDARD.md
  V06_TOKEN_NOISE_CONTROL.md
  V06_SKILL_ITERATION_PROTOCOL.md
templates/
  A_SOURCE_PACKET.md
  B_TOPIC_DECISION_CARD.md
  C_EVIDENCE_PACK.md
  D_STYLE_ROUTE_CARD.md
  E_DRAFT_PACKAGE.md
  F_PRODUCT_REVIEW_REPORT.md
  Z_ROUND_REVIEW.md
resources/
  style_cards/KOL_CARD_TEMPLATE.md
registry/
  AGENT_REGISTRY.md
  THREAD_ARCHIVE.md
.agents/skills/
  btm-z-orchestrator/
  btm-a-source-scout/
  btm-b-topic-gate/
  btm-c-evidence-data/
  btm-d-style-router/
  btm-e-draft-writer/
  btm-f-product-reviewer/
```

## Public Repository Boundaries

Do not commit:

- `local_registry/`
- `local_working/`
- `local_source/`
- `local_archive/`
- `runtime/`
- `raw_sources/`
- `daily_outputs/`
- `article_outputs/`
- raw article text, failed drafts, private user material, real thread IDs, or real local absolute paths

## Style Cards

KOL style cards are resources under `resources/style_cards/`. Do not create one Skill per KOL.
