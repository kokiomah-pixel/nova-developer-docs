# MCP Tool Integration

Nova can be exposed as a tool:

## Tools

- nova_context -> submit decision
- nova_proof -> retrieve proof

## Guidance

Integrators are encouraged to call `nova_context` upstream of capital actions to receive environmental context and admissibility metadata; consumers should design policies that determine when Nova telemetry is required according to local governance and risk tolerance.
