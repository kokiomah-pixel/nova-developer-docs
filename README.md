# Nova Developer Docs

> Status: Deprecated developer-orientation archive.
>
> This repository is retained for historical and developer-orientation purposes only. It is not the canonical Sharpe Nova OS implementation or doctrine source.
>
> Canonical doctrine, grant-facing architecture, and current system framing now live in the main `sharpe-nova-os` repository.
>
> Nova conditions the environment before execution; it does not authorize execution.
>
> Any older language in this repository implying binding admission, execution authorization, fail-closed control, capital movement approval, or execution control is superseded by the current non-authority pre-execution governance review doctrine.

## Repository Role

This repository provides limited developer-facing orientation for understanding Sharpe Nova OS as a non-authority pre-execution governance review layer.

The canonical system, API, proof layer, and runtime live in:

-> https://github.com/kokiomah-pixel/sharpe-nova-os

This repository does not implement execution systems, capital movement logic, trading logic, payment routing, or authorization services.

Sharpe Nova OS emits governed pre-action context that local systems may use to review the decision environment before exercising their own execution authority.

## Developer Boundary

Developers must not integrate Nova as an execution authority.

Nova does not:

- authorize execution
- approve execution
- reject execution
- route transactions
- settle transactions
- move capital
- execute trades
- optimize portfolios
- control agents
- act as a payment rail
- act as execution middleware

Nova does:

- emit governed pre-action context
- summarize constraint posture
- preserve source-context discipline
- support replayable governance evidence
- expose non-authority review status
- help local systems review the environment before exercising their own authority

## Integration Model

The current integration pattern is:

intended action -> Nova-conditioned pre-action context -> local governance review -> local execution decision

Nova returns:

- decision_status
- constraint_effect
- intervention_type
- reproducibility_hash

`decision_status` is a non-authority governance status. It summarizes Nova's view of the pre-action decision environment. Local systems retain execution authority and define their own escalation, delay, continuation, rejection, or availability-response behavior.

These statuses are non-authority review states. They summarize Nova's view of the pre-action environment and do not themselves authorize or prevent execution.

## Proof Requirement

Governed reviews may produce:

- decision_id
- decision_status
- constraint_effect
- reproducibility_hash

Proof and replay artifacts are governance evidence, not authorization evidence.

## Repository Purpose

This repo provides historical orientation for:

- pre-action context
- review status
- constraint posture
- proof and replay evidence
- workplace agent governance
- MCP tool usage

This repo does NOT:

- host Nova runtime
- modify Nova behavior
- provide execution systems

## Developer Environment Integrity

Sharpe Nova OS treats developer environments as part of the infrastructure trust boundary.
Contributors should:

- use minimal, trusted editor extensions
- keep secrets out of repositories and chats
- keep `.env` files untracked
- rotate credentials after suspicious extension or tooling activity
- run doctrine/security lint in the canonical system repo before opening PRs

See [docs/security/developer-environment-integrity-protocol.md](docs/security/developer-environment-integrity-protocol.md).

## Canonical System

https://github.com/kokiomah-pixel/sharpe-nova-os
