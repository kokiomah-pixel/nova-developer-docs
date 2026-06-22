# Field Hierarchy

This document is retained for developer-orientation continuity only.

Nova conditions the environment before execution; it does not authorize execution.

## Primary Review Fields

- decision_status
- constraint_effect
- intervention_type

## Secondary (Supporting)

- impact_on_outcomes
- adjustment

Primary fields summarize the pre-action review environment. They do not define execution behavior.

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or fail-closed behavior.
