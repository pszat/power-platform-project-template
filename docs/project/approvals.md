# Scoped approval record

No new implementation approval is supplied by this template.
Existing approved client policy belongs in `docs/agents/project.md`; this log
records task-level decisions and later changes without duplicating that policy.

For each real approval, add:

- Approval ID and status: proposed, approved, rejected, or superseded.
- Exact task/change scope, components, environment, and operations.
- Approver identity or permitted role alias, date, and retrievable evidence.
- Constraints, exclusions, approved deviations, and acceptance criteria.
- Superseding approval reference, if any.

A copied example, empty form, pending proposal, or asset upload is not approval.
User approval of a mockup does not authorize schema, integration, or access changes.
Do not repeatedly ask for an unchanged scope that is already explicitly approved.
If evidence cannot be retrieved or scope is unclear, stop only dependent work and
request a decision.

Keep evidence references client-permitted and free of secrets or sensitive payloads.
