# MCP Tool Integration

This document is retained for developer-orientation continuity only. It does not define new tool surfaces.

Nova conditions the environment before execution; it does not authorize execution.

Nova-conditioned context may be requested through existing local integration patterns:

- nova_context -> submit decision
- nova_proof -> retrieve proof

## Review Boundary

The current integration pattern is:

```text
intended action -> Nova-conditioned pre-action context -> local governance review -> local execution decision
```

Nova emits governed pre-action context for local review. It does not approve, route, settle, or execute actions.
