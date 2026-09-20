# Task Model

## Core fields

```yaml
id: stable task identity
outcome: observable result
current_state: confirmed facts only
next_action: one concrete move
next_actor: human | ai | collaborator
priority: today | this_week | scheduled | parked
wake_trigger: date, dependency, or external change
acceptance_criteria: evidence required for closure
source: where the task came from
status: active | waiting | blocked | done | cancelled
```

## Status rules

- `active`: a useful next action exists now.
- `waiting`: no useful action exists until a trigger.
- `blocked`: a next action exists, but access, input, or a decision is missing.
- `done`: the acceptance criteria are met with evidence.
- `cancelled`: the intended outcome is no longer needed.

Keep the same ID when wording, priority, or next actor changes. Create a new ID only when the intended outcome or acceptance criteria materially changes.

## Progress and acceptance

Progress evidence shows that an intermediate action happened. Acceptance evidence proves the intended result is usable.

Examples:

| Progress evidence | Possible acceptance evidence |
| --- | --- |
| Draft written | Reviewer confirms it is ready for use |
| Configuration saved | End-to-end test succeeds |
| Message sent | Recipient provides the required decision or artifact |
| Meeting completed | Agreed next step, owner, and evidence are recorded |

Never upgrade the left column to `done` unless it satisfies the task's own acceptance criteria.

## Priority selection

Daily outcomes should be corrected against the user's stated goals, commitments, deadlines, and active risks. If goals are absent, infer only from the supplied evidence and mark the basis.

Use no more than three daily outcomes. Sub-actions belong under the outcome instead of competing with it.

