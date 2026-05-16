# Coordination-Safe Enforcement

This document defines coordination-safe enforcement behavior for systems that integrate Sharpe Nova OS.

Sharpe Nova OS is a pre-execution environmental governance layer that emits derivative telemetry to help integrators condition their orchestration posture.

## Coordination Risk

Improper downstream behavior can amplify instability when multiple systems ignore admission discipline or react without governed enforcement.

## Integrator Guidance

Integrators are advised to:

- call Nova upstream of execution to receive admissibility metadata and coordination context
- treat `decision_status` as derivative telemetry for consumer interpretation and local governance
- translate `CONSTRAIN` outcomes into consumer-specific pacing/adjustments
- treat `DENY`, `DELAY`, `HALT`, and `VETO` as indicators of elevated constraint pressure that should prompt escalation or increased review rather than being treated as a remote execution permit
- preserve proof-backed records for governed actions and correlate telemetry with consumer decisions

## Prohibited Behavior

Integrators should not:

- bypass Nova for speed or convenience without assessing telemetry and risk
- treat internal reasoning as permission
- synchronize around denial-state retries without higher-fidelity checks
- execute before applying appropriate local admission conditioning

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Methodology & Change Control](methodology-change-control.md)
- [Continuous Decision Loop](docs/continuous_decision_loop.md)

Sharpe Nova OS  
Guidance for coordination-safe integration and consumer-responsibility enforcement patterns.
