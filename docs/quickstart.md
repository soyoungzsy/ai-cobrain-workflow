# Quick Start

## Before you begin

Use a small, sanitized sample. Do not paste confidential messages, personal data, credentials, internal links, or unreleased business information into an AI service unless your organization explicitly allows it.

## Step 1 — Prepare raw input

Collect tasks from one project or the last one to three days. Plain text is enough:

```text
- Prepare next week's customer interview outline.
- Design draft is ready; someone needs to test the real signup link.
- Finance will reply on Friday. No action before that.
- Compare three public research tools and summarize trade-offs.
```

## Step 2 — Run the prompt

Copy [`prompts/cobrain-secretary.md`](../prompts/cobrain-secretary.md), append the raw input, and send it to your AI assistant.

## Step 3 — Correct four fields

Do not rewrite everything. Check only:

1. **Priority** — are the proposed daily outcomes actually important?
2. **Next actor** — who can make the next useful move?
3. **Wake trigger** — when should a waiting task return?
4. **Acceptance criteria** — what observable evidence proves completion?

## Step 4 — Save the workbench

Use [`templates/daily-workbench.md`](../templates/daily-workbench.md). Keep a separate [`task-ledger.md`](../templates/task-ledger.md) if you want waiting and scheduled tasks to persist across days.

## Step 5 — Calibrate at day end

Tell the AI:

```text
Review today's plan. Identify one priority mistake, one routing mistake,
and one completion judgment that should change tomorrow.
Propose rules, but do not save them as permanent preferences until I confirm.
```

Run this manually for seven days before adding automation.

## 关联

- [Architecture](architecture.md)
- [Calibration guide](calibration-guide.md)
- [Fictional workday](../examples/fictional-workday.md)

## 来源与证据

- The steps intentionally avoid platform-specific integrations so beginners can test the method safely.

## 修改记录

- 2026-09-19: Initial quick start.
