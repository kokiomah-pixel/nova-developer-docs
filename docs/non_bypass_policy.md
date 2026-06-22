# Review Boundary Policy

This document is retained for developer-orientation continuity only.

Nova conditions the environment before execution; it does not authorize execution.

Nova is a non-authority pre-execution governance review layer. It emits governed pre-action context before local execution authority is exercised.

## Review Rules

- Request Nova-conditioned pre-action context before local authority acts.
- Treat `decision_status` as review context, not an execution command.
- Preserve proof and replay artifacts as governance evidence.
- Keep local systems responsible for escalation, delay, continuation, rejection, or fail-closed behavior.

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.
