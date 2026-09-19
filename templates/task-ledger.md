# Task Ledger

The ledger preserves task identity when an item leaves the daily frontstage.

| ID | Outcome | Status | Next actor | Wake trigger | Acceptance criteria | Last verified |
| --- | --- | --- | --- | --- | --- | --- |
| T-001 |  | active | human |  |  |  |

## Status vocabulary

- `active`: a useful next action exists;
- `waiting`: no action until a trigger;
- `blocked`: action exists but access, input, or a decision is missing;
- `done`: acceptance evidence is met;
- `cancelled`: the outcome is no longer needed.

## Identity rule

Keep the same ID when wording, priority, or next actor changes. Create a new ID only when the intended outcome or acceptance criteria materially changes.

## 关联

- [Architecture](../docs/architecture.md)
- [Daily workbench](daily-workbench.md)

## 来源与证据

- Empty public template; no real task identifiers included.

## 修改记录

- 2026-09-19: Initial public template.
