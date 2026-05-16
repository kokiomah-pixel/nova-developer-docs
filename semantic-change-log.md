Semantic Change Log — doctrine-alignment-2026-05-16

1) file/path: docs/openai_workspace_agents.md
   original language:
   - "Nova determines if those actions are admissible."
   - "Agent -> Decision Proposal -> Nova -> Execution"
   - "decision_status is binding"
   - "ALLOW -> execute  CONSTRAIN -> adjust, then execute  DENY / DELAY / HALT / VETO -> do not execute"
   updated language:
   - "Nova emits admissibility telemetry describing environmental context for proposed actions."
   - "Agent -> Decision Proposal -> Nova (environmental context) -> Consumer orchestration & execution (consumer remains responsible for decisions)"
   - "decision_status is derivative telemetry that consumers should interpret according to local governance."
   - "Example consumer interpretations (non-normative): ALLOW indicates lower constraint pressure — a consumer may choose to proceed after applying local safeguards; CONSTRAIN suggests local adjustments or pacing; DENY / DELAY / HALT / VETO signal elevated constraint pressure and should trigger stricter review or escalation rather than be treated as a sovereign fiat."
   rationale:
   - Remove prescriptive gating language; reframe Nova as telemetry emitter.
   doctrine alignment objective:
   - Teach integrators to treat Nova outputs as environmental context rather than execution authority.
   sovereignty implications:
   - Preserves Nova internal reasoning and prevents treating telemetry as internal explanation.
   developer interpretation impact:
   - Developers will design local governance to interpret telemetry rather than mechanically enforcing execution gates.
   unresolved risks:
   - If internal teams used these docs for binding runbooks, update runbooks separately.
   risk level: HIGH

2) file/path: coordination-safe-enforcement.md
   original language:
   - "Integrators must: - call Nova before execution - enforce `decision_status` as binding - apply `CONSTRAIN` outcomes exactly as returned - block execution on `DENY`, `DELAY`, `HALT`, and `VETO`"
   updated language:
   - "Integrator guidance: - call Nova upstream of execution to receive admissibility metadata and coordination context - treat `decision_status` as derivative telemetry for consumer interpretation and local governance - translate `CONSTRAIN` into consumer-specific pacing/adjustments - treat `DENY`, `DELAY`, `HALT`, and `VETO` as indicators of elevated constraint pressure that should prompt escalation or increased review rather than being treated as a remote execution permit"
   rationale:
   - Remove “must/enforce/block” language that implies external sovereign authority.
   doctrine alignment objective:
   - Make Nova clearly an environmental governance surface.
   sovereignty implications:
   - Avoids external inference of Nova reasoning or authority.
   developer interpretation impact:
   - Encourages building local escalation/inspection routines.
   unresolved risks:
   - Potential mismatch with compliance-runbooks; logged for review.
   risk level: HIGH

3) file/path: docs/non_bypass_policy.md
   original language:
   - "Nova is a required pre-execution checkpoint."
   - "Nova must be called before any capital-moving action"
   - "decision_status is authoritative"
   - "No execution without Nova admission"
   - "Fail-Closed Behavior: If Nova is unavailable: -> execution must NOT proceed"
   updated language:
   - "Nova is an upstream environmental conditioning checkpoint that emits derivative telemetry."
   - "Integrators should call Nova upstream of capital-moving actions to receive admissibility metadata."
   - "decision_status is derivative telemetry intended for consumer interpretation and local governance."
   - "Consumers should avoid bypassing Nova environmental context when local governance requires upstream conditioning."
   - "Fail-Closed guidance: Some operators choose a fail-closed posture if Nova is unavailable; consumers must design failover/availability policies appropriate to their governance and risk tolerance."
   rationale:
   - Convert absolute enforcement language to recommended guidance.
   doctrine alignment objective:
   - Prevent misassignment of execution authority.
   sovereignty implications:
   - No exposure of internal logic.
   developer interpretation impact:
   - Forces explicit design of local failover policies.
   unresolved risks:
   - Operational policies that mandated fail-closed behavior may need alignment; recorded in unresolved-risks-and-actions.md.
   risk level: HIGH

4) file/path: docs/continuous_decision_loop.md
   original language:
   - "intent -> size -> Nova -> decision_status -> execution (only if admitted)"
   - "This loop must occur before EVERY capital-moving action."
   updated language:
   - "intent -> size -> Nova (environmental context) -> Consumer orchestration & execution (consumer remains responsible for decisions)"
   - "Nova returns derivative telemetry (decision_status) that consumers should interpret; systems should incorporate this telemetry into their local enforcement and pacing logic. Recommended upstream integration of this loop prior to capital-moving actions where appropriate."
   rationale:
   - Remove "only if admitted" gating phrasing; reframe as telemetry-first.
   doctrine alignment objective:
   - Emphasize Nova as a conditioning surface.
   sovereignty implications:
   - Avoids implying Nova grants execution authority.
   developer interpretation impact:
   - Encourages consumer-side interpretation.
   unresolved risks:
   - If teams rely on this as a hard compliance check, they must be notified.
   risk level: HIGH

5) file/path: docs/proof_layer_integration.md
   original language:
   - "Every Nova decision produces a proof record."
   - "Proof must be retrieved after decision execution."
   updated language:
   - "Every Nova emission produces a proof record of the derived telemetry."
   - "Proof should be retrieved and correlated with consumer actions for audit and reproducibility; retrieval is part of consumer audit workflows and does not itself convey execution authority."
   rationale:
   - Clarify proof is for audit, not an execution permit.
   doctrine alignment objective:
   - Prevent misinterpretation of proof as authorization.
   sovereignty implications:
   - None significant.
   developer interpretation impact:
   - Encourages audit correlations without implying permission.
   unresolved risks:
   - Minor; safe to apply.
   risk level: MEDIUM

6) file/path: docs/field_hierarchy.md
   original language:
   - "Primary (Authoritative) ... Primary fields define execution behavior."
   updated language:
   - "Primary (Telemetry) ... Primary fields provide derivative telemetry and admissibility metadata for consumer interpretation; they inform consumer execution posture but do not themselves confer execution authority."
   rationale:
   - Remove wording that frames fields as authoritative executors.
   doctrine alignment objective:
   - Clarify role of schema keys as telemetry.
   sovereignty implications:
   - None beyond clarifying external surface.
   developer interpretation impact:
   - Avoids misunderstanding that schema keys are execution commands.
   unresolved risks:
   - None significant.
   risk level: MEDIUM

7) file/path: docs/mcp_tool_integration.md
   original language:
   - "All capital actions must call nova_context before execution."
   updated language:
   - "Integrators are encouraged to call `nova_context` upstream of capital actions to receive environmental context and admissibility metadata; consumers should design policies that determine when Nova telemetry is required according to local governance and risk tolerance."
   rationale:
   - Change imperative to guidance.
   doctrine alignment objective:
   - Enforce telemetry-first design while preserving consumer decision authority.
   sovereignty implications:
   - None.
   developer interpretation impact:
   - Promotes upstream conditioning without imposing runtime mandate in docs.
   unresolved risks:
   - If tooling expects the prior strict mandate, update coordination notes.
   risk level: MEDIUM

8) file/path: developer-responsibilities.md
   original language:
   - "All integrators must: - call Nova before any capital-moving action - bind execution behavior to `decision_status` - refuse execution on `DENY`, `DELAY`, `HALT`, and `VETO` - If Nova is unavailable, execution must not proceed."
   updated language:
   - "Recommended integrator responsibilities: - call Nova upstream of capital-moving actions to receive admissibility metadata - interpret `decision_status` as derivative telemetry and incorporate it into local enforcement and safeguards - treat `DENY`, `DELAY`, `HALT`, and `VETO` as indicators of elevated constraint pressure and escalate or increase review according to local governance - When Nova is unavailable, consumers must design failover/availability policies appropriate to local risk tolerance (some operators adopt a fail-closed posture)."
   rationale:
   - Replace prescriptive language with consumer-responsibility guidance.
   doctrine alignment objective:
   - Avoid treating Nova as a granting authority.
   sovereignty implications:
   - Preserves Nova internals.
   developer interpretation impact:
   - Forces explicit local governance decision-making and failover planning.
   unresolved risks:
   - Potential divergence with prior organizational mandates; add to unresolved-risks-and-actions.md for stakeholder sync.
   risk level: HIGH


All changes are prose-only and preserve schema keys, endpoints, runtime behavior, and SDK compatibility. Any code-like examples detected were left unchanged and recorded in unresolved-risks-and-actions.md for manual review.
