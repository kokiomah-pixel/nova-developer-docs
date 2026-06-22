# OpenAI Workspace Agent Integration

This document is retained for developer-orientation continuity only.

Nova conditions the environment before execution; it does not authorize execution.

Workspace agents may form intended actions. Nova emits governed pre-action context that local systems may review before local execution authority is exercised.

## Required Flow

```text
intended action -> Nova-conditioned pre-action context -> local governance review -> local execution decision
```

## Rules

- Request Nova-conditioned pre-action context before local authority acts.
- Treat `decision_status` as a non-authority governance status, not an execution command.
- Preserve proof and replay artifacts as governance evidence.
- Keep local policy responsible for continuation, escalation, delay, rejection, or fail-closed behavior.

## Status Handling

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.
