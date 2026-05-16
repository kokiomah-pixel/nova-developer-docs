# Nova Developer Responsibilities

This document defines the responsibilities of developers, agents, protocols, and institutions integrating Sharpe Nova OS.

Sharpe Nova OS is a pre-execution environmental governance layer that emits derivative telemetry to condition consumer orchestration.

## Integrator Responsibilities

Recommended integrator responsibilities:

- call Nova upstream of capital-moving actions to receive admissibility metadata
- interpret `decision_status` as derivative telemetry and incorporate it into local enforcement and safeguards
- translate `CONSTRAIN` outcomes into consumer-specific pacing/adjustments before considering execution
- treat `DENY`, `DELAY`, `HALT`, and `VETO` as indicators of elevated constraint pressure and escalate or increase review according to local governance
- retain `decision_id` for governed actions
- retrieve proof when audit, verification, or governance review is required and correlate it with consumer decisions

## Non-Bypass Duty

Integrators should not:

- treat Nova output as a substitute for local governance
- override refusal-state telemetry without documented rationale and higher-fidelity checks
- retry decisions solely to force `ALLOW` outcomes; prefer adaptive pacing or human review

## Fail-Closed Guidance

When Nova is unavailable, consumers must design failover and availability policies appropriate to their governance and risk tolerance. Some operators choose a fail-closed posture; others implement compensating controls. Document your chosen posture and ensure it aligns with organizational risk policies.

## Related Documents

- [Methodology & Change Control](methodology-change-control.md)
- [Coordination-Safe Enforcement](coordination-safe-enforcement.md)
- [Non-Bypass Policy](docs/non_bypass_policy.md)

Sharpe Nova OS  
Developer integration doctrine for upstream environmental governance and derivative telemetry consumption.
