# Power Automate standard

Justify automation against app logic and Dataverse mechanisms for the actual
requirement. Create solution-aware flows in the approved unmanaged DEV solution.
Follow approved environment-variable and connection-reference usage where supported
and justified.

Before implementation, identify:

- Trigger, filtering/execution conditions, inputs/outputs, and business side effects.
- Flow owner, connector identities, run-only user behavior where applicable,
  connection references, permissions, and personal-connection dependencies.
- Licensing/DLP restrictions, sensitive fields, and diagnostic access.
- Retry policy, timeouts, failure reporting/recovery, concurrency, and duplicate
  handling at the business-operation boundary.

Do not assume exactly-once execution. Where repeated effects matter, choose and
approve a safe re-execution/idempotency strategy. Consider partial success before
retries or resubmission; a failed run may already have changed data.

Introducing a developer's personal connection requires explicit agreement.
Authentication and ownership changes are not implied by permission to edit a flow.

Inspect existing definitions and dependencies before editing. Validate the
definition using available tooling, and test runtime behavior with approved test
data and side effects. Run validation is distinct from definition validation.
Publish/enable/run/resubmit only within approved operation scope; do not leave
unapproved active triggers or test resources.

Record flow IDs, trigger context, references, execution identities, failure
handling, and verification evidence in the registry and component documentation.
