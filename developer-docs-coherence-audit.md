Developer Docs Coherence Audit — doctrine-alignment-2026-05-16

Checklist (post Phase A+B)

- Landing/Intro: updated (README)
- Continuous Decision Loop: reframed (docs/continuous_decision_loop.md) — DONE
- Quickstarts/onboarding: TODO — full scan scheduled
- API reference phrasing: TODO — plan created in api-reference-framing-sync-notes.md
- Examples & payloads: TODO — scan for code-like gating examples (flagged)
- Integration Philosophy: added (docs/integration-philosophy.md) — DONE
- Sovereignty Boundaries: added (docs/sovereignty-boundaries.md) — DONE
- Glossary: added (docs/glossary.md) — DONE
- FAQ: added (docs/faq.md) — DONE

Applied Phase A+B edits (prose-only):
- docs/continuous_decision_loop.md
- docs/proof_layer_integration.md
- docs/field_hierarchy.md
- docs/mcp_tool_integration.md
- developer-responsibilities.md (narrative sections)
- docs/openai_workspace_agents.md
- coordination-safe-enforcement.md
- docs/non_bypass_policy.md

Notes:
- No runtime, endpoint, schema key, or SDK changes were performed.
- Code snippets and pseudo-code were NOT modified; any such occurrences flagged in unresolved-risks-and-actions.md.

Next steps:
- Run a secondary automated scan for remaining instances of deprecated verbs in the repo and produce a prioritized patch list for non-prose items.
- Coordinate with compliance/ops for any documentation that is used in binding runbooks before converting absolute enforcement language in those artifacts.
