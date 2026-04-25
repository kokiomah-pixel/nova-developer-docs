# Nova Developer Responsibilities

This document defines the responsibilities of developers, agents, protocols, and institutions integrating Sharpe Nova OS.

Sharpe Nova OS is a pre-execution decision discipline layer.

## Integrator Responsibilities

All integrators must:

- call Nova before any capital-moving action
- bind execution behavior to `decision_status`
- apply `CONSTRAIN` outcomes before execution
- refuse execution on `DENY`, `DELAY`, `HALT`, and `VETO`
- retain `decision_id` for governed actions
- retrieve proof when audit, verification, or governance review is required

## Non-Bypass Duty

Integrators must not:

- treat Nova output as non-binding
- override refusal states with internal heuristics
- retry decisions to force `ALLOW`
- execute without decision admission

## Fail-Closed Duty

If Nova is unavailable, execution must not proceed.

## Related Documents

- [Methodology & Change Control](methodology-change-control.md)
- [Coordination-Safe Enforcement](coordination-safe-enforcement.md)
- [Non-Bypass Policy](docs/non_bypass_policy.md)

Sharpe Nova OS  
Developer integration doctrine for pre-execution decision admission
