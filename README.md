# Power Platform project

This repository includes an agent instruction starter, not a configured application.

## First use

1. Read [AGENTS.md](AGENTS.md), then run the
   [onboarding procedure](docs/agents/onboarding.md) in the actual repository.
2. Confirm [project policy](docs/agents/project.md); replace template decisions
   with approved project choices rather than assuming defaults are approvals.
3. Populate the [non-secret registry](docs/project/registry.md) from verified facts
   and approved decisions. Follow [local setup](docs/project/local-setup.md) for
   workstation-specific authentication.
4. Supply permitted approved assets through the
   [Canvas reference catalog](references/canvas/README.md).
5. Implement only after the relevant target, approvals, dependencies, and
   verification route are confirmed.

Suggested first prompt:

> Read AGENTS.md and run first-use onboarding. Inspect available project facts
> before asking grouped questions. Report blockers and safe next actions. Do not
> create cloud resources, alter schemas, connect new services, or commit until the
> corresponding scope is authorized.

## Optional Matt Pocock workflow

Run `/setup-matt-pocock-skills` after the real repository/tracker is reachable.
Preserve `AGENTS.md`. Configure root `GLOSSARY.md` and `docs/decisions/` as the domain
documentation locations; create them only when terms or decisions warrant it.

Then use discovery, specifications, end-to-end tickets, and implementation as
appropriate. Skills do not override the project approval gates, including commit
authorization. No skills, labels, or GitHub resources are created by these files.

## Source and verification

Agree the supported app authoring and solution-source workflow before editing.
Keep approved reference assets distinct from working files and solution exports.
Local YAML edits do not prove an application has changed.

Follow [delivery gates](docs/agents/delivery.md). These templates have not verified
any live environment, app, flow, or permissions.
