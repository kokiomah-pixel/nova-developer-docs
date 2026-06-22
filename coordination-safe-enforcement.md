# Coordination-Safe Review

> Status: Superseded terminology notice.
>
> This file previously used enforcement-oriented language. The current Sharpe Nova OS doctrine treats Nova as a non-authority pre-execution governance review layer.
>
> Nova conditions the environment before execution; it does not authorize execution.
>
> Nova does not enforce, authorize, approve, reject, route, settle, or execute actions.

This document is retained for developer-orientation continuity only.

## Coordination Risk

Improper downstream behavior can amplify instability when multiple systems treat review context as an execution command or compress local policy into Nova output.

## Coordination-Safe Review Pattern

Nova supports coordination-safe review by emitting pre-action context before local execution authority is exercised.

The review pattern is:

```text
agentic workflow forms intended action
-> Nova emits pre-action governance context
-> local system reviews authority scope, constraint posture, source context, and replay evidence
-> local system decides whether to continue, delay, escalate, or stop under its own policy
```

Nova does not make the execution decision.

Nova makes the decision environment reviewable.

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Methodology & Change Control](methodology-change-control.md)
- [Continuous Decision Loop](docs/continuous_decision_loop.md)

Sharpe Nova OS  
Coordination-safe review orientation for coordinated capital systems
