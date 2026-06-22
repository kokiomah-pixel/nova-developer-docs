# Continuous Decision Loop

This document is retained for developer-orientation continuity only.

Nova conditions the environment before execution; it does not authorize execution.

The current review pattern is:

```text
intended action -> Nova-conditioned pre-action context -> local governance review -> local execution decision
```

## Example

1. Agent proposes allocation
2. System requests Nova-conditioned pre-action context
3. Nova returns review context and `decision_status`
4. Local governance policy reviews the context
5. Local system makes its own execution decision
6. Proof and replay artifacts are stored as governance evidence

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.
