# Nova Methodology & Change Control

This document defines how Sharpe Nova OS methodology changes without weakening decision admission, proof integrity, or non-bypass enforcement.

Sharpe Nova OS is a pre-execution decision discipline layer.

## Change Control Principles

Methodology changes must preserve:

- authoritative `decision_status`
- proof-backed governance
- reproducibility
- fail-closed integration doctrine

## Rules

1. Historical records remain immutable.
2. New methodology applies only to future decisions or future published versions.
3. Version changes must be published explicitly.
4. Integrators must receive migration documentation when response interpretation changes.
5. No change may weaken binding pre-execution enforcement or make Nova bypassable.

## Integrator Expectation

Integrators must continue to:

- call Nova before execution
- bind execution behavior to returned primary fields
- retrieve proof from the proof endpoint when required

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Coordination-Safe Enforcement](coordination-safe-enforcement.md)
- [Proof Layer Integration](docs/proof_layer_integration.md)

Sharpe Nova OS  
Methodology governance for binding decision admission
