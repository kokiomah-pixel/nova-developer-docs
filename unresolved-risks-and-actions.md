Unresolved Risks and Actions - doctrine-alignment-2026-05-16

1) Flagged code-like examples and operational runbooks (do NOT auto-change):

- Any code snippets that implement enforcement logic (e.g., conditional statements like `if decision_status == ALLOW then execute`) were left unchanged. Review list:
  - (no explicit code-block files detected in this pass; if found later, they will be added here)

2) Compliance and runbook alignment:

- Files that previously used imperative 'must' language and may be referenced by organizational policy were converted to guidance. Confirm with compliance/ops that these documentation changes do not conflict with contractual or policy obligations.

3) Additional scan required:

- Quickstarts, API reference pages, and sample apps need a focused textual pass to identify any remaining inference of Nova as execution authority. Action: schedule follow-up commits for narrative-only edits after manual review of flagged items.

4) Items deferred for manual review:

- Any examples embedded in third-party sample apps or binary fixtures that appear to implement gating logic.

All items above are recorded so the Chief Coherence Officer can review and authorize any further changes requiring stakeholder signoff.
