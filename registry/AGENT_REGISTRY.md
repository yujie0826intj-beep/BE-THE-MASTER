# AGENT_REGISTRY

## V06 Public Registry

This file is safe for a public repository. Real local paths and real thread IDs are stored only in `local_registry/`, which must stay ignored by git.

Current project root alias: `<PROJECT_ROOT>`

Legacy root alias: `<LEGACY_FINANCE_ROOT>`; historical reference only, no new writes.

## V06 Role Registry

| Role | Public session label | Thread ref | Skill | Status | Current task | Notes |
|---|---|---|---|---|---|---|
| Z | Z_ORCHESTRATOR | local-only | `btm-z-orchestrator` | idle | V06-FREEZE-RESTRUCTURE-20260703 | Current orchestration entry; no draft production |
| A-V06 | unassigned | none | `btm-a-source-scout` | idle/unassigned | none | Create only after user starts V06 test |
| B-V06 | unassigned | none | `btm-b-topic-gate` | idle/unassigned | none | Owns GO/PIVOT/KILL |
| C-V06 | unassigned | none | `btm-c-evidence-data` | idle/unassigned | none | Must return to B when evidence is insufficient |
| D-V06 | unassigned | none | `btm-d-style-router` | idle/unassigned | none | Style route only, not final review |
| E-V06 | unassigned | none | `btm-e-draft-writer` | idle/unassigned | none | One revision max per round |
| F-V06 | unassigned | none | `btm-f-product-reviewer` | idle/unassigned | none | Must output PROCESS and PRODUCT conclusions |

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
6. New V06 tests must start from `Z -> A`, not directly from E drafting.

## Private Registry

Real path and thread details must stay in local-only ignored registry files.
