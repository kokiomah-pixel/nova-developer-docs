# Nova Developer Responsibilities

This document is retained for developer orientation only. Canonical doctrine lives in the main `sharpe-nova-os` repository.

Nova conditions the environment before execution; it does not authorize execution.

Developers integrating Sharpe Nova OS should request Nova-conditioned pre-action context before local execution authority is exercised in high-stakes agentic financial workflows.

Nova does not authorize or execute actions. Local systems retain authority and must define their own policies for escalation, delay, rejection, continuation, or fail-closed behavior.

## Integrator Responsibilities

Developer responsibilities include:

1. Request Nova-conditioned pre-action context before local authority acts.
2. Preserve the returned context for review and replay.
3. Treat `decision_status` as a non-authority governance status, not an execution command.
4. Maintain local policy for whether to continue, delay, escalate, or stop.
5. Preserve source segmentation and replay artifacts when available.
6. Avoid using Nova as a callable utility detached from the pre-execution review boundary.

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.

## Integration Warning

Do not reduce Nova to a utility function.

The superseded integration pattern is:

```text
call Nova -> execute if allowed
```

The current integration pattern is:

```text
intended action -> Nova-conditioned pre-action context -> local governance review -> local execution decision
```

## Related Documents

- [Methodology & Change Control](methodology-change-control.md)
- [Coordination-Safe Review](coordination-safe-enforcement.md)
- [Non-Bypass Policy](docs/non_bypass_policy.md)

Sharpe Nova OS  
Developer orientation for non-authority pre-execution governance review
