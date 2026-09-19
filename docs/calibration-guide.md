# Seven-Day Calibration Guide

The prompt is only a starting point. The useful system emerges when your judgment becomes explicit.

| Day | Focus | Question to correct |
| --- | --- | --- |
| 1 | Capture | Did the AI merge duplicates without losing real differences? |
| 2 | Outcomes | Did it choose results, or merely list meetings and actions? |
| 3 | Routing | Is the next actor correct for every active task? |
| 4 | Waiting | Which tasks appeared before any useful action was possible? |
| 5 | Acceptance | Which task was closed with weak evidence? |
| 6 | Noise | What did the AI surface that did not deserve attention? |
| 7 | Learning | Which rules are stable enough to keep? |

## Four common failure modes

### Everything becomes “today”

Correction: require a real action condition and cap daily outcomes at three.

### Actions are mistaken for outcomes

Correction: rewrite “meet”, “send”, and “review” as the observable change those actions should create.

### Owners and deadlines are guessed

Correction: mark missing information as `unconfirmed`; never infer formal ownership from proximity in a conversation.

### Tasks close too early

Correction: separate progress evidence from acceptance evidence. “Configured” may be progress; “tested end to end” may be acceptance.

## Minimal evaluation

For five consecutive workdays, record:

- frontstage task count;
- backstage task count;
- duplicate or unnecessary reminders;
- false-completion catches;
- tasks independently completed by AI;
- where released attention was reinvested.

Avoid claiming productivity gains without a baseline and consistent definitions.

## 关联

- [Core prompt](../prompts/cobrain-secretary.md)
- [Architecture](architecture.md)

## 来源与证据

- The failure modes are generalized from real use and contain no organization-specific examples.

## 修改记录

- 2026-09-19: Initial calibration guide.
