# OpenAI Workspace Agent Integration

Workspace agents may propose actions.

Nova emits admissibility telemetry describing environmental context for proposed actions.

## Required Flow

Agent -> Decision Proposal -> Nova (environmental context) -> Consumer orchestration & execution (consumer remains responsible for decisions)

## Rules

- Agents should call Nova upstream of execution to receive environmental telemetry and admissibility metadata
- `decision_status` is derivative telemetry that consumers should interpret according to local governance
- Agents may not treat Nova internal reasoning as permission
- Agents should retrieve proof when required for audit or verification

## Outcome Handling

Example consumer interpretations (non-normative):

- ALLOW: indicates lower constraint pressure; a consumer may choose to proceed only after applying local safeguards and local governance
- CONSTRAIN: suggests local adjustments or pacing; consumers should translate constraint_effect into appropriate pacing or review
- DENY / DELAY / HALT / VETO: indicate elevated constraint pressure; consumers should escalate, increase review, defer, or apply stricter local safeguards according to local governance

Note: Do not interpret these examples as prescriptive code. Consumers are responsible for implementing their own governance, failover, and escalation policies.
