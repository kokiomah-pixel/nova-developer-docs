# Non-Bypass Policy

Nova is an upstream environmental conditioning checkpoint that emits derivative telemetry.

## Rules

- Integrators should call Nova upstream of capital-moving actions to receive admissibility metadata
- `decision_status` is derivative telemetry intended for consumer interpretation and local governance
- DENY / DELAY / HALT / VETO indicate elevated constraint pressure and should be handled via increased review, escalation, or local safeguards rather than treated as a sovereign ban
- CONSTRAIN should be translated into consumer-specific adjustments before considering execution
- Avoid retry strategies that attempt to bypass constraint signals; prefer adaptive pacing or human review

## Fail-Closed Guidance

When Nova is unavailable, many operators choose a fail-closed posture; consumers must design failover and availability policies appropriate to their governance and risk tolerance.
