# Coordination-Safe Guidance

**Document Version:** v1.0  
**Applies to:** Nova Constitution v1.x

Sharpe Nova OS provides regime classification and advisory context for capital systems.

Nova is designed to improve decision awareness while avoiding coordinated behavior that may destabilize markets.

---

# The Coordination Problem

If many systems react identically to a signal, markets can become unstable.

Examples include:

- synchronized liquidations
- mass liquidity withdrawals
- abrupt capital exits

Nova is intentionally designed to **avoid triggering coordinated actions**.

---

# Recommended Integrator Behavior

Integrators should prefer gradual adjustments rather than abrupt responses.

Examples of coordination-safe behavior:

- throttle deployment pace
- tighten exposure limits
- scale down leverage
- pause new risk gradually

These behaviors preserve systemic stability.

---

# Behaviors to Avoid

Systems integrating Nova should avoid:

- automatic full-portfolio exits
- synchronized liquidity withdrawals
- hard liquidation triggers
- cliff-edge capital responses

These behaviors can amplify market instability.

---

# Risk-Adaptive Systems

Nova works best when used inside systems that adapt gradually.

Examples include:

- dynamic exposure scaling
- staged liquidity deployment
- progressive risk reduction

---

# Human Oversight

Where possible, Nova signals should be combined with:

- human review
- governance processes
- system-level safeguards

Human oversight reduces the risk of unintended coordination effects.

---

# Design Philosophy

Nova exists to:

- improve decision awareness
- encode historical consequence
- support resilient capital systems

Nova does **not exist to coordinate market behavior**.

---

## Related Documents

- [Developer Responsibilities](developer-responsibilities.md)
- [Methodology & Change Control](methodology-change-control.md)

---

Sharpe Nova OS  
Decision-context infrastructure for autonomous capital systems
