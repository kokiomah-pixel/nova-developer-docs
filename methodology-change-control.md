# Nova Methodology & Change Control

This document defines how Sharpe Nova OS evolves while preserving system stability, reproducibility, and integrator trust.

Sharpe Nova OS is designed to behave as **durable decision-context infrastructure** for autonomous capital systems.

Methodology changes must be predictable, transparent, and non-disruptive to systems that depend on Nova.

---

# Core Concepts

## Epoch

Nova operates on discrete time intervals called **epochs**.

Each epoch produces a finalized regime classification that describes the current capital environment.

An epoch typically includes:

- timestamp
- regime classification
- constitution version
- verification signature

Once finalized, epoch outputs are **immutable**.

Historical epochs must never be modified.

This immutability ensures:

- auditability
- reproducibility
- stable downstream integrations

---

## Regime Taxonomy

Nova classifies market environments using a structured regime taxonomy.

Example regimes include:

- Stable  
- Elevated Fragility  
- Stress  

The taxonomy provides a simplified representation of systemic risk conditions affecting capital deployment.

Regime classifications represent **environmental context**, not predictions.

They are intended to inform decision posture rather than forecast outcomes.

---

# Constitution Version

Nova operates under a defined **constitution version**.

The constitution version specifies the methodology used to produce regime classifications.

This includes:

- regime definitions
- classification rules
- signal interpretation boundaries
- telemetry weighting assumptions

Example:
