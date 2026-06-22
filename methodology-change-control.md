# Methodology Change Control

This document is retained for developer-orientation continuity only. Canonical doctrine lives in the main `sharpe-nova-os` repository.

## Doctrine Preservation Rule

All methodology changes must preserve the non-authority boundary:

```text
Nova conditions the environment before execution; it does not authorize execution.
```

Methodology updates must not introduce language implying that Nova:

- approves execution
- denies execution
- authorizes capital movement
- controls execution paths
- controls agents
- routes or settles transactions
- acts as an execution gate

## Change-Control Review

Before accepting any methodology change, review whether it alters Nova's layer.

Acceptable changes may clarify:

- pre-action context
- review status
- constraint posture
- source segmentation
- replay evidence
- local authority separation

Unacceptable changes imply:

- Nova decides whether capital moves
- Nova is the execution authority
- `decision_status` is an execution command
- downstream systems must obey Nova as a controller

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Coordination-Safe Review](coordination-safe-enforcement.md)
- [Proof Layer Integration](docs/proof_layer_integration.md)

Sharpe Nova OS  
Methodology governance for non-authority pre-execution review
