# Nova Methodology & Change Control

This document defines the governance framework under which Sharpe Nova OS evolves.

Sharpe Nova OS is designed to function as **durable decision-context infrastructure for capital systems**.  
As such, methodological stability, reproducibility, and transparent change management are core design priorities.

This document explains how Nova methodology may evolve without disrupting systems that depend on Nova outputs.

---

# Core Concepts

## Epoch

Nova operates on discrete time intervals called **epochs**.

Each epoch produces a finalized regime classification representing the systemic capital environment at that time.

Each epoch record includes:

- timestamp
- regime classification
- constitution version
- verification metadata

Once finalized, epoch outputs are **immutable**.

Historical epochs are never modified.

This immutability ensures:

- reproducibility
- auditability
- deterministic historical analysis

---

## Regime Taxonomy

Nova represents the capital environment through a structured regime taxonomy.

Example regimes include:

- **Stable**  
- **Elevated Fragility**  
- **Stress**

These regimes describe **systemic market conditions**, not forecasts.

They encode environmental risk context derived from historical consequence patterns and market fragility signals.

Regime classifications are intended to inform **capital posture decisions**, not predict price movements.

---

# Constitution Version

Nova operates under a defined **constitution version**.

The constitution version identifies the methodology used to produce regime classifications.

The constitution defines:

- regime definitions
- signal weighting logic
- classification thresholds
- telemetry interpretation rules
- fragility detection logic

Example:
