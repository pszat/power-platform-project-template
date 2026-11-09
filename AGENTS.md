# Power Platform agent instructions

## Read before work

Read [project policy](docs/agents/project.md) and the
[project registry](docs/project/registry.md) before project work.
For first use, incomplete setup, or changed accounts/environments, follow
[onboarding](docs/agents/onboarding.md) before affected implementation.

Load all references triggered by the task, not just one:

| Task | Required reading before implementation |
|---|---|
| Planning, editing, testing, committing, exporting, or delivery | [Delivery](docs/agents/delivery.md) |
| Canvas screens, controls, Power Fx, themes, or navigation | [Canvas](docs/agents/canvas.md) and [asset index](references/canvas/README.md) |
| Tables, columns, relationships, permissions, files, or persistent state | [Data and security](docs/agents/data-security.md) |
| Flows, triggers, connectors, or service connections | [Automation](docs/agents/automation.md) and [data and security](docs/agents/data-security.md) |
| Authentication or workstation configuration | [Local setup](docs/project/local-setup.md) |

## Non-negotiable boundaries

- Verify the authenticated account, tenant, and environment against approved
  registry targets before writes. An environment display name is insufficient.
- Default writes to explicitly approved development targets. Other environments
  require explicit project scope and operation approval.
- Approve schema, security, integration, licensing, destructive, and significant
  behavior/design changes before implementing them unless their exact scope is
  already approved. Model approval does not authorize deletion or migration.
- Use least privilege; protect secrets and sensitive data in every artifact.
- Distinguish facts, proposals, assumptions, approvals, and unverified claims.
  Inspect available evidence; report unavailable evidence without inventing it.
- A missing dependency blocks affected work, not independent analysis.
- Project policy specializes the baseline. Report contradictions for a decision;
  neither a skill nor a generic workflow silently removes approval gates.

## Completion

Follow the delivery verification gates. Local files, a successful command, or a
commit alone are not proof that platform behavior works.
