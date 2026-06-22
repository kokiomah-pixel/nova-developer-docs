# Proof Layer Integration

This document is retained for developer-orientation continuity only.

Nova conditions the environment before execution; it does not authorize execution.

Nova review may produce a proof record.

## Required Fields

- decision_id
- decision_status
- constraint_effect
- reproducibility_hash

## Usage

- audit
- verification
- governance tracking
- replay evidence

Proof and replay artifacts are governance evidence, not authorization evidence.

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.
