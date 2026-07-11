# SKILL_CHANGELOG

Public-safe record of reusable V06 skill and template changes. Do not record real thread IDs, local absolute paths, private source text, article bodies, or raw materials here.

## 2026-07-11

### V06-HANDOFF-AND-CONTEXT-HYGIENE

- Change type: handoff contract, template completion, and token-noise control.
- Decision: make A hand only `SOURCE_READY_FOR_S` packets to S; add a public `B_CONFIRM_CARD` template; require B confirmation before D/E; prefer compact F inputs; archive wrong-root or context-compacted role threads before new production.
- Reason: the locked chain already required S and B confirmation, but A's Skill/template and several public summaries still encoded the older A-to-B route. Long-lived role threads also caused avoidable context rehydration.
- Files changed:
  - `.agents/skills/btm-a-source-scout/SKILL.md`
  - `.agents/skills/btm-d-style-router/SKILL.md`
  - `.agents/skills/btm-e-draft-writer/SKILL.md`
  - `.agents/skills/btm-f-product-reviewer/SKILL.md`
  - `.agents/skills/btm-z-orchestrator/SKILL.md`
  - `templates/A_SOURCE_PACKET.md`
  - `templates/B_CONFIRM_CARD.md`
  - `templates/D_STYLE_ROUTE_CARD.md`
  - `templates/E_DRAFT_PACKAGE.md`
  - `templates/F_PRODUCT_REVIEW_REPORT.md`
  - `templates/Z_ROUND_REVIEW.md`
  - `README.md`
  - `AGENTS.md`
  - `docs/V06_WORKFLOW.md`
  - `docs/V06_ROLE_BOUNDARY.md`
  - `docs/V06_QUALITY_GATES.md`
  - `docs/V06_TOKEN_NOISE_CONTROL.md`
  - `registry/THREAD_ARCHIVE.md`
- Public-safe summary: new source work cannot skip S, D cannot start without B_CONFIRM, F should consume compact locked handoffs, and context-heavy role threads are archive-only.
- Not preserved: article text, private paths, real thread IDs, user source material, or old full-thread content.

## 2026-07-04

### V06-S-ROLE-INTRODUCTION

- Change type: role and workflow update.
- Decision: add S-V06 as an independent signal-analysis role between A-V06 and B-V06.
- Reason: prevent the workflow from jumping from source collection to topic judgment without forming a reporter-style judgment from abnormal signals.
- Files changed:
  - `.agents/skills/btm-s-signal-analyst/SKILL.md`
  - `templates/S_THICK_DESCRIPTION_CARD.md`
  - `AGENTS.md`
  - `docs/V06_ARCHITECTURE.md`
  - `docs/V06_WORKFLOW.md`
  - `docs/V06_ROLE_BOUNDARY.md`
  - `docs/V06_PRODUCT_PASS_STANDARD.md`
  - `docs/V06_TOKEN_NOISE_CONTROL.md`
  - `.agents/skills/btm-z-orchestrator/SKILL.md`
  - `.agents/skills/btm-b-topic-gate/SKILL.md`
  - `.agents/skills/btm-f-product-reviewer/SKILL.md`
  - `templates/B_TOPIC_DECISION_CARD.md`
  - `templates/Z_ROUND_REVIEW.md`
  - `registry/AGENT_REGISTRY.md`
- Public-safe summary: A scouts sources; S converts abnormal signals into a thick-description judgment candidate; B validates and decides `GO/PIVOT/KILL`; C/D/E/F proceed only if upstream gates pass.
- Private details: none recorded here.

### BTM-V06-S-LEARN-001-ACCEPTED

- Change type: S method upgrade.
- Decision: upgrade `.agents/skills/btm-s-signal-analyst/SKILL.md`.
- Reason: accepted learning round showed that S needs explicit rules for abnormal signal definition, material thickness, and one-sentence reporter judgment formation.
- Files changed:
  - `.agents/skills/btm-s-signal-analyst/SKILL.md`
- Public-safe summary: An abnormal signal must diverge from normal business expectations, constrain future choices, and be supported by a sufficient evidence cluster before S hands a judgment candidate to B.
- Not preserved: article facts, source text, KOL wording, titles, openings, paragraph rhythm, or full writing style.

## 2026-07-05

### S_STRUCTURAL_JUDGMENT_GATE

- Change type: mandatory S gate and downstream routing update.
- Decision: add `S_STRUCTURAL_JUDGMENT_GATE` before B topic judgment.
- Reason: S must not form a thesis from thin A material or isolated facts. S judgment must come from a macro/policy/industry or business-model frame, enough independent signals, a mechanism, a falsifier, and clear causal boundaries.
- Files changed:
  - `.agents/skills/btm-s-signal-analyst/SKILL.md`
  - `.agents/skills/btm-z-orchestrator/SKILL.md`
  - `.agents/skills/btm-b-topic-gate/SKILL.md`
  - `.agents/skills/btm-c-evidence-data/SKILL.md`
  - `templates/S_THICK_DESCRIPTION_CARD.md`
  - `templates/B_TOPIC_DECISION_CARD.md`
  - `templates/C_EVIDENCE_PACK.md`
  - `AGENTS.md`
  - `docs/V06_QUALITY_GATES.md`
  - `docs/V06_WORKFLOW.md`
  - `docs/V06_ROLE_BOUNDARY.md`
- Public-safe summary: If S cannot pass the structural judgment gate, Z must stop the route and either return to A for more source depth, ask the user for human reporter judgment, or close the signal. B and C must not continue from a thin or unformed S judgment.
- Not preserved: article facts, source text, user private materials, thread IDs, or draft text.

### BTM-V06-CHAIN-LOCK-001

- Change type: workflow, template, and skill floor update.
- Decision: lock the first post-S chain that produced a user-recognized quality improvement as the current minimum production baseline.
- Reason: prevent future writing from regressing to the pre-S pattern where B/C/D/E tried to repair a thin or unformed judgment through repeated gates and rewrites.
- Files changed:
  - `docs/V06_LOCKED_GENERATION_CHAIN.md`
  - `docs/V06_ARCHITECTURE.md`
  - `docs/V06_WORKFLOW.md`
  - `docs/V06_ROLE_BOUNDARY.md`
  - `docs/V06_QUALITY_GATES.md`
  - `docs/V06_PRODUCT_PASS_STANDARD.md`
  - `docs/V06_TOKEN_NOISE_CONTROL.md`
  - `AGENTS.md`
  - `templates/E_DRAFT_PACKAGE.md`
  - `templates/F_PRODUCT_REVIEW_REPORT.md`
  - `templates/Z_ROUND_REVIEW.md`
  - `.agents/skills/btm-e-draft-writer/SKILL.md`
  - `.agents/skills/btm-f-product-reviewer/SKILL.md`
  - `.agents/skills/btm-z-orchestrator/SKILL.md`
- Public-safe summary: Default route now requires S before B, B confirmation after C, E micro sample before full draft when the route is new or repaired, and F comparison against `BTM-V06-FINAL-001`. Pre-S production attempts are quarantined as noise or failure examples.
- Not preserved: article body, source text, real thread IDs, private local paths, or user private materials.
