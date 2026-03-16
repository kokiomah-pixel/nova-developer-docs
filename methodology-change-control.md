# Nova Methodology & Change Control

**Document Version:** v1.0  
**Applies to:** Nova Constitution v1.x

This document defines the governance framework under which Sharpe Nova OS evolves.

Nova is designed to function as durable decision-context infrastructure for capital systems.

Methodology changes must be predictable, transparent, and non-disruptive.

---

# Core Concepts

## Epoch

Nova operates on discrete time intervals called **epochs**.

Each epoch produces a finalized regime classification representing the systemic capital environment.

Each epoch record includes:

- timestamp
- regime classification
- constitution version
- verification metadata

Once finalized, epoch outputs are **immutable**.

Historical epochs are never modified.

---

## Regime Taxonomy

Nova represents the capital environment through a structured regime taxonomy.

Example regimes include:

- Stable
- Elevated Fragility
- Stress

These regimes describe systemic market conditions rather than price predictions.

---

# Constitution Version

Nova operates under a defined **constitution version**.

The constitution version specifies the methodology used to produce regime classifications.

Example:
The constitution version allows integrators to trace which methodology generated a classification.

---

# Methodology Evolution

Nova methodology may evolve as market structures change and research advances.

Triggers may include:

- structural changes in liquidity systems
- improved systemic risk detection
- improved telemetry coverage

---

# Methodology Change Rules

All methodology updates must obey these constraints:

1. Historical epochs remain immutable
2. New methodology applies only to future epochs
3. Version changes are explicitly published
4. Major revisions include migration documentation

---

# Versioning Policy

Nova methodology uses semantic versioning.

Example:
Version interpretation:

| Version | Meaning |
|--------|--------|
| Patch | Minor correction |
| Minor | Incremental improvement |
| Major | Structural methodology revision |

---

# Deprecation Policy

If a telemetry source or rule becomes obsolete:

1. Deprecation notice is published
2. Integrators receive advance notice
3. Migration guidance is provided
4. Historical epochs remain unchanged

---

# Governance Principles

Nova methodology governance prioritizes:

**Stability**  
Changes should minimize disruption.

**Transparency**  
Changes must be documented.

**Auditability**  
Historical outputs must remain verifiable.

**Predictability**  
Integrators must be able to anticipate changes.

---

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Coordination-Safe Guidance](coordination-safe-guidance.md)

---

Sharpe Nova OS  
Decision-context infrastructure for autonomous capital systems
