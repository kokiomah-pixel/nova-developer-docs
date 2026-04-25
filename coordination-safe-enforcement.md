# Coordination-Safe Enforcement

This document defines coordination-safe enforcement behavior for systems that integrate Sharpe Nova OS.

Sharpe Nova OS is a pre-execution decision discipline layer.

## Coordination Risk

Improper downstream behavior can amplify instability when multiple systems ignore admission discipline or react without governed enforcement.

## Required Enforcement Posture

Integrators must:

- call Nova before execution
- enforce `decision_status` as binding
- apply `CONSTRAIN` outcomes exactly as returned
- block execution on `DENY`, `DELAY`, `HALT`, and `VETO`
- preserve proof-backed records for governed actions

## Prohibited Behavior

Integrators must not:

- bypass Nova for speed or convenience
- treat internal reasoning as permission
- synchronize around denial-state retries
- execute before admission

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Methodology & Change Control](methodology-change-control.md)
- [Continuous Decision Loop](docs/continuous_decision_loop.md)

Sharpe Nova OS  
Binding enforcement doctrine for coordinated capital systems
