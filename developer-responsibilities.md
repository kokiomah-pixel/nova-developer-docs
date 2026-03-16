
# Nova Developer Responsibilities

This document defines the responsibilities and expectations for developers, agents, protocols, and institutions integrating Sharpe Nova OS.

Sharpe Nova OS provides **decision context infrastructure** for capital systems.

Nova does **not** execute capital actions.

Integrators remain fully responsible for all downstream capital decisions.

---

# Nova Guarantees

Nova guarantees the following properties.

## Deterministic Regime Classification

Nova produces a canonical regime state for each epoch.

Example regimes include:

- Stable  
- Elevated Fragility  
- Stress  

Once finalized, regime classifications for an epoch are **immutable**.

---

## Advisory Guardrails

Nova may provide advisory guardrails describing market conditions.

Guardrails:

- are informational signals  
- provide contextual risk guidance  
- do not enforce execution constraints  

Nova never blocks or forces capital actions.

---

## Historical Intelligence

Nova exposes historical regime and transition information.

This information represents **encoded historical consequences**, not predictive forecasts.

Historical information may be used for:

- research  
- system design  
- risk modeling  
- simulations  

---

## Verifiability

Nova responses may include:

- signatures  
- hashes  
- optional onchain anchors  

These allow integrators to verify that regime outputs are authentic and untampered.

---

# What Nova Does Not Do

Nova explicitly does **not**:

- execute trades  
- rebalance portfolios  
- control treasury allocations  
- block transactions  
- enforce strategy decisions  

Nova is a **decision-support system only**.

Execution systems remain external to Nova.

---

# Integrator Responsibilities

Developers integrating Nova must:

- treat Nova outputs as advisory signals  
- maintain independent risk management systems  
- avoid automatic execution based solely on Nova signals  
- implement monitoring and safeguards  

Nova should be used as one component of a broader decision process.

---

# Risk Disclaimer

Nova does not provide investment advice.

Nova signals should not be interpreted as instructions to:

- buy assets  
- sell assets  
- deploy liquidity  
- withdraw capital  

All capital decisions remain the responsibility of the integrating system or operator.

---

# Responsible Use

Integrators are encouraged to design systems that:

- scale risk gradually  
- reduce exposure under stress  
- avoid abrupt market reactions  

Nova is designed to improve **decision awareness**, not to coordinate market behavior.

---

Sharpe Nova OS  
Decision-context infrastructure for autonomous capital system
