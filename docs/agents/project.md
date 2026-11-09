# Project policy: configure before affected implementation

Status: unconfigured template, not an approved architecture.

This baseline targets Canvas Apps, Dataverse, and Power Automate. Choose actual
components according to requirements; inclusion in the stack does not justify
creating a flow or resource.

## Decisions to collect

Use the [onboarding procedure](onboarding.md) and record:

- Business purpose, actors, application language, device/browser requirements,
  accessibility needs, expected volumes, and acceptance criteria.
- In-scope environments and operations, approved accounts, owners, and solution.
- Persistent data ownership and lifecycle. Dataverse is the baseline business
  data platform; any different business data store requires an explicit decision.
- File storage, record/file relationships, access rules, and failure handling.
  No file-storage provider is selected by this template.
- Schema naming, publisher configuration, security model, and integration rules.
- Approved UI assets and the design/mockup approval workflow.
- Supported authoring, source-control, export/import, and runtime verification.
- Repository/tracker, branch and review rules, and commit authorization.

## Approval rules

The baseline approval gates in the entry point remain in force. Select
project-specific design gates explicitly; this template imposes neither a
particular screen template nor mandatory HTML mockups on every project.

Until approved targets and scope exist, analysis and local document drafting may
continue, but affected cloud writes remain blocked.

Record approved policy decisions here, resource facts in the
[registry](../project/registry.md), and approval evidence in the
[approval log](../project/approvals.md). Do not mark proposals as approved.
