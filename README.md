# Power Platform project

This repository includes an agent instruction starter, not a configured application.

## Install the template repository

These are instructions and reference folders, not an executable application.
There is no package installation or build step.

### Publish the starter on GitHub

1. Create a repository on [GitHub](https://github.com/new). For a reusable public
   template, include only generic material; keep client information private.
2. Upload the contents of the starter folder into the repository root, not the
   enclosing `reusable-starter` folder or ZIP. On an empty repository use
   **uploading an existing file**; otherwise use **Add file > Upload files**.
3. Include hidden folders/files such as `.github/` and `.gitignore`. Confirm this
   root structure before committing:

   ```text
   AGENTS.md
   README.md
   .gitignore
   .github/
     agents/
       power-platform-expert.agent.md
     skills/
       power-platform-architect/
         SKILL.md
   docs/
   references/
   solutions/
   ```

4. Review the upload for secrets and client-specific information, then commit.
   Do not upload the client overlay to a generic public template.
5. In **Settings > General**, enable **Template repository**.

When adding this starter to an existing repository, merge instructions and
`.gitignore` deliberately. Preserve existing project files and approved rules.

### Create a new project from the template

1. Open the template repository and select **Use this template > Create a new
   repository**.
2. Choose the owner and project name. Use a **private** repository for client
   projects unless public access is explicitly approved.
3. Create the repository. This creates an independent copy; later template changes
   will not automatically update it.
4. In VS Code, run **Git: Clone** from the Command Palette, paste the new project
   repository URL, choose a local folder, and open the cloned folder.
   Git and authorized GitHub access are needed for cloning private repositories.
5. Follow the first-use procedure below in the new project, not in the generic
   template. Add client policy/assets only after checking storage permissions.

### Verify GitHub Copilot discovery

1. Use a current VS Code installation with GitHub Copilot Chat available and an
   authorized GitHub account. Follow organizational workspace-trust policies.
2. Open the repository root, not only an individual Markdown file. Confirm the
   agent host supports root `AGENTS.md` and workspace skills/custom agents.
3. Open Copilot Chat and select **Power Platform Expert** from the agent picker.
4. Type `/` and look for `power-platform-architect`, or explicitly ask Copilot to
   use that skill. If discovery is missing, inspect customization diagnostics and
   host settings/support; reload the VS Code window after adding files if needed.
5. Test without writes:

   > Read AGENTS.md. Use power-platform-architect to summarize the approved scope
   > and list missing onboarding decisions. Do not change files or cloud resources.

6. Confirm the response respects the project policy and identifies unknown registry
   values rather than inventing accounts, IDs, assets, or approvals.

Select your preferred model in Copilot; the included agent does not pin one.
See [customization guidance](docs/agents/customizations.md) for details.

### Configure platform tools separately

Copying these files does not install Power Platform CLI, Matt Pocock plugins,
Canvas Authoring MCP, Power Automate tooling, connectors, or licenses. It also
does not sign in to a tenant or create an app/solution.

During onboarding, identify only the tools needed for the planned work and follow
their current official setup instructions. Obtain required installation,
connection, and resource approvals. Authenticate through approved sign-in flows;
never put credentials in the registry or chat. Verify the actual account, tenant,
environment, and resource before writes.

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

## Included specialist customizations

The starter includes a Power Platform architecture skill and expert agent under
`.github/`. See [installation, usage, and provenance](docs/agents/customizations.md).
These files do not install platform connections or replace project instructions.

## Optional Matt Pocock workflow

Run `/setup-matt-pocock-skills` after the real repository/tracker is reachable.
Preserve `AGENTS.md`. Configure root `GLOSSARY.md` and `docs/decisions/` as the domain
documentation locations; create them only when terms or decisions warrant it.

Then use discovery, specifications, end-to-end tickets, and implementation as
appropriate. Skills do not override the project approval gates, including commit
authorization. No Matt Pocock plugins, labels, or GitHub resources are installed
or created by these files.

## Source and verification

Agree the supported app authoring and solution-source workflow before editing.
Keep approved reference assets distinct from working files and solution exports.
Local YAML edits do not prove an application has changed.

Follow [delivery gates](docs/agents/delivery.md). These templates have not verified
any live environment, app, flow, or permissions.
