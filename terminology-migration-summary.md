Terminology Migration Summary - doctrine-alignment-2026-05-16

Preferred terms (canonical):
- environmental governance
- environmental context
- derivative telemetry
- coordination context
- admissibility environment
- constraint pressure
- pacing condition
- drift
- fragmentation
- pulse
- temporal governance
- orchestration stabilization

Deprecated / Avoid in docs:
- allow, deny, approval, rejection, execution authorization, trading signal, recommendation, prediction, portfolio optimizer, execution decision

Applied mapping examples:
- "decision_status is binding" -> "decision_status is derivative telemetry for consumer interpretation and local governance"
- "ALLOW -> execute" -> "ALLOW indicates lower constraint pressure; a consumer may choose to proceed only after applying local safeguards and local governance"
- "Nova must be called before execution" -> "Nova should be called upstream of execution to receive environmental context and admissibility metadata"

Note: Schema keys remain unchanged; only surrounding descriptive language was updated.
