# AGENT_REGISTRY

## V06 Public Registry

This file is safe for a public repository. Real local paths and real thread IDs are stored only in `local_registry/`, which must stay ignored by git.

Current project root alias: `<PROJECT_ROOT>`

Legacy root alias: `<LEGACY_FINANCE_ROOT>`; historical reference only, no new writes.

## V06 Role Registry

| Role | Public session label | Thread ref | Skill | Status | Current task | Notes |
|---|---|---|---|---|---|---|
| Z | Z_ORCHESTRATOR | local-only | `btm-z-orchestrator` | idle/accepted | BTM-V06-CHAIN-LOCK-001 | Post-S chain locked as current baseline; pre-S noise quarantined |
| A-V06 | A_SOURCE_SCOUT | none | `btm-a-source-scout` | idle/unassigned | none | Wrong-root/context-heavy predecessor archived; create a clean replacement only for an authorized task |
| S-V06 | S_SIGNAL_ANALYST | none | `btm-s-signal-analyst` | idle/unassigned | BTM-V06-SB-REPLAY-002 | Accepted S gate remains historical evidence; predecessor thread archived |
| B-V06 | B_TOPIC_GATE | none | `btm-b-topic-gate` | idle/unassigned | BTM-V06-B-CONFIRM-001 | Accepted B and B_CONFIRM outputs remain historical evidence; predecessor thread archived |
| C-V06 | C_EVIDENCE_DATA | none | `btm-c-evidence-data` | idle/unassigned | BTM-V06-C-DIAGNOSTIC-001 | Accepted diagnostic remains historical evidence; predecessor thread archived |
| D-V06 | D_STYLE_ROUTER | none | `btm-d-style-router` | idle/unassigned | BTM-V06-D-REROUTE-001 | Accepted reroute remains historical evidence; predecessor thread archived |
| E-V06 | E_DRAFT_WRITER | none | `btm-e-draft-writer` | idle/unassigned | BTM-V06-E-CONTROLLED-DRAFT-001 | Accepted controlled draft remains baseline evidence; predecessor thread archived |
| F-V06 | F_PRODUCT_REVIEWER | none | `btm-f-product-reviewer` | idle/unassigned | BTM-V06-F-REVIEW-001 | Accepted review remains baseline evidence; predecessor thread archived |

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
