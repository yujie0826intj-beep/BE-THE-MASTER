# AGENT_REGISTRY

## V06 Public Registry

This file is safe for a public repository. Real local paths and real thread IDs are stored only in `local_registry/`, which must stay ignored by git.

Current project root alias: `<PROJECT_ROOT>`

Legacy root alias: `<LEGACY_FINANCE_ROOT>`; historical reference only, no new writes.

## V06 Role Registry

| Role | Public session label | Thread ref | Skill | Status | Current task | Notes |
|---|---|---|---|---|---|---|
| Z | Z_ORCHESTRATOR | local-only | `btm-z-orchestrator` | idle/accepted | BTM-V06-CHAIN-LOCK-001 | Post-S chain locked as current baseline; pre-S noise quarantined |
| A-V06 | A_SOURCE_SCOUT_01 | local-only | `btm-a-source-scout` | idle/registered | none | Real thread id stored only in `local_registry/`; no task dispatched |
| S-V06 | S_SIGNAL_ANALYST_01 | local-only | `btm-s-signal-analyst` | idle/accepted | BTM-V06-SB-REPLAY-002 | S structural gate passed; B small replay allowed |
| B-V06 | B_TOPIC_GATE_01 | local-only | `btm-b-topic-gate` | idle/accepted | BTM-V06-B-CONFIRM-001 | B_CONFIRM completed: GO on narrowed question; D allowed only after user confirmation |
| C-V06 | C_EVIDENCE_DATA_01 | local-only | `btm-c-evidence-data` | idle/accepted | BTM-V06-C-DIAGNOSTIC-001 | C diagnostic completed: EVIDENCE_SUPPORTS_NARROWER_PIVOT; no B_CONFIRM/D/E/F dispatch |
| D-V06 | D_STYLE_ROUTER_01 | local-only | `btm-d-style-router` | idle/accepted | BTM-V06-D-REROUTE-001 | D reroute completed: STYLE_ROUTE_READY; stopped before E |
| E-V06 | E_DRAFT_WRITER_01 | local-only | `btm-e-draft-writer` | idle/accepted | BTM-V06-E-CONTROLLED-DRAFT-001 | Controlled full draft passed Z gate; stopped before F |
| F-V06 | F_PRODUCT_REVIEWER_01 | local-only | `btm-f-product-reviewer` | idle/accepted | BTM-V06-F-REVIEW-001 | F completed: PROCESS_PASS and PRODUCT_PASS; returned to Z for human final acceptance |

## V05/R6 Freeze

| Item | Status | Public note |
|---|---|---|
| V05/R6 | frozen | Process pass, user rejected product quality |
| C/D micro-fixes | blocked | No further dispatch |
| heartbeat patrol | disabled/not_found | No active `btm-b` automation found |
| Legacy root writes | forbidden | Historical reference only |
| Long old-thread rehydrate | forbidden | Use V06 public architecture files only |

## Status Values

- `idle/unassigned`: V06 role has no current thread.
- `idle`: no active task.
- `active`: processing a clear task; max one per role.
- `waiting_upstream`: waiting for upstream handoff.
- `blocked`: needs Z or user decision.
- `archived`: historical thread, never dispatch.
- `deprecated`: historical skill or workflow entry, not for V06.

## Dispatch Rules

1. Dispatch only to current V06 registered role threads.
2. Do not use archived V05 A/B/C/D threads as substitutes.
3. Do not revive old abnormal or recovery B threads.
4. Z may perform at most one state-changing action per patrol.
5. Do not run heartbeat automation.
6. New V06 tests must start from `Z -> A -> S`, not directly from B or E drafting.

## Private Registry

Real path and thread details must stay in local-only ignored registry files.
