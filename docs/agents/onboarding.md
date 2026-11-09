# First-use onboarding

Run on first use and after material changes to targets, accounts, assets, or tools.
Setup is complete for a task only when its required facts, permissions, approvals,
dependencies, and verification path are confirmed. A completed template is not
proof that a connection works.

## 1. Inspect before asking

Read project policy, registry, approval log, existing instructions, repository
remote, solution metadata, agreed decisions, and available approved references.
Check available tool versions, authentication status, and exposed connection
metadata using authorized read-only operations.

Retrieve only necessary metadata. Do not read credential stores or output tokens,
cookies, passwords, sensitive run payloads, or unrelated account information.
Do not install tools, switch accounts/environments, or connect to a new service
silently. A new connection requires the relevant permission and integration approval.

Record discoverable facts with source and verification date. Report inaccessible
information as unknown; do not ask the user to retrieve facts already accessible
through authorized tools.

## 2. Collect decisions in dependency order

Ask a grouped round of independent questions; wait before asking questions whose
answers depend on that round. Give recommended answers without approving them.
Collect only what is needed for the planned scope:

1. Purpose, owners, actors, scenarios, exclusions, language, devices, volumes,
   acceptance criteria, data classification, and permitted documentation.
2. Tenant, approved DEV target, account/role selection, solution and publisher,
   resource-creation authority, and available licenses/DLP constraints.
3. Data/file storage and access, schema changes, integrations and execution
   identities, concurrency/duplicate behavior, and error/recovery expectations.
4. UI baseline, screen states, approved assets, mockup/design approval process,
   supported editing method, and runtime verification.
5. Source-control workflow, shared editing ownership, tracker, commits, reviews,
   and what evidence closes a task.

Do not collect actual account identities or tenant metadata in tracked files until
the client permits that information to be stored there. A role alias plus an
approved secure lookup can be used instead. Never request credentials in chat.

## 3. Populate the information repository

- [Registry](../project/registry.md): non-secret resource facts, approved identity
  selection, constraints, tools, and readiness, with evidence and date.
- [Approval log](../project/approvals.md): exact authorized changes, approver,
  evidence, exclusions, and superseding decisions.
- [Asset index](../../references/canvas/README.md): actual approved files and
  their provenance, dependencies, and permitted adaptations.
- [Local setup](../project/local-setup.md): shared workstation procedure; keep
  actual machine paths/profile names under ignored `.local/`.
- Root glossary: agreed business definitions only, created when terms resolve.
  Architectural trade-offs belong in `docs/decisions/`, created when warranted.

Use `unknown` for missing facts, `pending creation` for approved-but-nonexistent
resources, and `not applicable` with a reason. Do not fabricate IDs or links.
Documenting a resource does not authorize creating it.

## 4. Verify readiness for the next operation

Before cloud writes, verify account/tenant/environment and approved operation scope.
For each service involved, inspect the actual connection context; the Studio user,
Dataverse caller, flow owner, run-only user, and connector identity may differ.

| Work | Required evidence before affected write |
|---|---|
| Solution/schema | Approved DEV target, authorized caller, solution/publisher, approved exact schema change, impact/security review |
| Canvas | Correct app/target, supported authoring path, required assets/data dependencies, required design approvals |
| SharePoint/files | Approved site/library, caller and access model, record/file mapping and partial-failure handling |
| Flow | Correct environment, trigger/side effects, connection references and execution identities, approved scope |
| Commit/export | Approved workflow, source ownership, inspected diff/export, secret/sensitive-data review |

A missing app ID need not block an approved new-app creation; verify the creation
target first, then record the returned ID. Apply the same rule to other new resources.
Read-only inspection must still respect access and data-handling restrictions.

## 5. Report and maintain

Report verified facts, decisions still needed, blockers by task, and the next safe
action. Never label the whole project ready when only some components were checked.
Reverify the active target before each logical write batch and after any context
switch; update the registry after approved resource creation or replacement.
