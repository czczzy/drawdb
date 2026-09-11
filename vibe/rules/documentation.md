# Project Documentation Rules

Tool: codex
Date: 2026-06-12

## Purpose

This file maps the CodeNote master rules to this repository without copying the master.

## Master Authorities

- Process layout and task date grouping: [CodeNote process rules](../../../../../czz/CzzProj/CodeNote/AiRef/VibePractice/Vibe_Rules/process/rules.md#3-project-location).
- AI-DB workspace shape, storage, and naming: [CodeNote DB governance](../../../../../czz/CzzProj/CodeNote/DevelopRef/调试工具/db/governance/README.md#5-workspace-shape-and-naming).

## Rule Entry Order

1. Read [../../AGENTS.md](../../AGENTS.md).
2. Read [README.md](README.md).
3. Read this file for documentation tiers, medium+ work, DB/data, cross-repo flow, deploy gates, or legacy docs.
4. Read [../specs/PROJECT_STATUS.md](../specs/PROJECT_STATUS.md) when it exists and the task is medium+, long-running, cross-repo, DB/data, deploy-gated, or business-changing.

## Documentation Tiers

| Tier | Path | Use |
| --- | --- | --- |
| Project rules | `vibe/rules/` | Project-specific stack, commands, risk gates, business rules, release rules |
| Process hub | `vibe/specs/PROJECT_STATUS.md` | Current main line, active task index, verification state, open gates, sibling links |
| Task docs | `vibe/specs/` | Task docs follow the CodeNote process layout authority above |
| Knowledge | `vibe/knowledge/` | Reusable project facts, ADR, glossary, error memory |
| DB workspace | `vibe/ai-db/` | Create only when DB/data workflows appear; storage and naming follow CodeNote DB governance |
| Legacy docs | project-defined | Historical analysis only; link to current authoritative docs when touched |

## Task Thresholds

- Small local fixes may skip task docs but must report verification and memory routing.
- Medium+ or business-changing work creates or updates task docs and verification records.
- DB/data work follows CodeNote DB governance and keeps plan, SQL, verification, and handoff records separate.
- Deploy-gated work records ordered deploy steps, blocking conditions, and rollback notes before recommending deploy.

## Cross-Repo Authority

- Backend/code: this repository unless a sibling status hub says otherwise.
- DDL/data: this repository when `vibe/ai-db/` exists; otherwise confirm before DB/data work and initialize through CodeNote DB governance.
- UI: this repository when it contains the UI implementation; otherwise link the sibling repo hub.
- Release/deploy: confirm project-specific path before deploy-related changes.
- Sibling status hubs: record links in [../specs/PROJECT_STATUS.md](../specs/PROJECT_STATUS.md) when cross-repo work starts.

## Closeout

- Update [../specs/PROJECT_STATUS.md](../specs/PROJECT_STATUS.md) when current focus, active task docs, verification, gates, sibling links, or memory routing changes.
- Promote reusable conclusions to `vibe/knowledge/`, ADR, project rules, or DB memory.
- Keep legacy docs linked, not duplicated as new authority.
