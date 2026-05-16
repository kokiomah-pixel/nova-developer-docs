# Continuous Decision Loop

All systems should operate with Nova as an upstream environmental conditioning surface:

intent -> size -> Nova (environmental context) -> Consumer orchestration & execution (consumer remains responsible for decisions)

## Example

1. Agent proposes allocation
2. System calls Nova (receives derivative telemetry)
3. Nova returns decision_status (derivative telemetry)
4. System interprets telemetry and applies local governance and safeguards
5. Proof is stored and correlated with consumer actions for audit

Recommended practice: integrate this loop upstream of capital-moving actions where appropriate so consumer orchestration can condition pacing, review, and safeguards based on Nova telemetry.
