# Power Platform project

This repository includes an agent instruction starter, not a configured application.

## Start here

These are instructions and reference folders, not an executable application.
There is no package installation, build step, or terminal setup command.

- **Starting a project from an existing GitHub template?** Follow steps 1-4 below.
- **Already cloned this project?** Start at step 2.
- **Publishing your own reusable template?** Follow
  [Publish the starter on GitHub](#publish-the-starter-on-github) first.

## 1. Create your project repository

1. On GitHub, open the template repository.
2. Select **Use this template > Create a new repository**.
3. Choose the owner and project name. Use a **private** repository for client
   projects unless public access is explicitly approved.
4. Create the repository. This is an independent copy; later template changes
   will not automatically update it.

## 2. Clone and open the correct folder

1. Install Git and VS Code if needed. For the standard Copilot experience, enable
   GitHub Copilot Chat and sign in with an authorized GitHub account.
2. In VS Code, open the Command Palette with **Ctrl+Shift+P**, run **Git: Clone**,
   and paste your **new project repository's** URL, not the template URL.
3. Select **Open** when cloning finishes. If already cloned, use
   **File > Open Folder** and choose the actual repository root.
4. In Explorer, confirm `AGENTS.md`, `README.md`, `docs`, and `.github` are directly
   inside the opened folder. Do not open only a Markdown file, the parent folder
   containing several repositories, or an enclosing starter-package folder.
5. Follow your organization's workspace-trust policy before enabling agent access.

For example, if the files are in
`C:\Projects\my-project\AGENTS.md` and `C:\Projects\my-project\.github`,
open `C:\Projects\my-project`, not `C:\Projects`.

## 3. Start first-use onboarding

Open a **new chat** in the project workspace. A special agent picker is not
required; the chat agent must be able to read repository files.

### Option A: Your chat supports repository skill commands

Type `/` and select **power-platform-onboarding**, or enter:

```text
/power-platform-onboarding
```

In standard VS Code Copilot Chat, `/skills` can also open the skills configuration
menu. Selecting **Power Platform Expert** is optional when your host offers it.

### Option B: The skill is missing from the menu, or you use an SDK chat host

Paste this message:

```text
Read .github/skills/power-platform-onboarding/SKILL.md and execute its
onboarding procedure now. Check whether you have minimum information for
my first task, then ask only for missing essentials, one short question
at a time.
```

Use **execute**, not only **read**: reading the file alone does not request
onboarding. This fallback runs the documented workflow; it does not register a
slash command. If the agent cannot read the file, fix workspace/file access first.

### What should happen

The agent checks existing records, asks only missing essentials for the current
task, and gives a short hint with each question. It requests confirmation before
saving project records. You do not need to complete the whole registry upfront:
additional information is collected when a later task needs it.

Onboarding does not create cloud resources, install tools, create connections,
commit, or push. Never supply passwords or tokens. See the authoritative
[onboarding procedure](docs/agents/onboarding.md).

## 4. Start project work

Tell the agent your first task, unless already supplied. It checks the relevant
prerequisites and reports the next safe action. Missing future details do not
block local planning; affected cloud operations wait for verified targets and
required approvals.

Review the [project policy](docs/agents/project.md) for your project. Add client
policy and assets only where storage is permitted; do not copy another client's
policy unchanged into a new project.

## If skills do not appear after typing `/`

1. Confirm the file exists at
   `.github\skills\power-platform-onboarding\SKILL.md` under the opened root.
   Root `skills\` is not the standard discovery location. The expert agent belongs
   under `.github\agents\`, not root `agents\`.
2. Run **Developer: Reload Window** from the Command Palette, start a new chat,
   and try `/` again.
3. In standard Copilot Chat, inspect `/skills` and customization diagnostics.
   Loading `AGENTS.md` or selecting an expert agent does not prove skills loaded.
4. If still missing, check your chat host's repository-skill support. SDK-based
   extensions may have different discovery and command menus. Use option B above
   when file access works; moving the file cannot add unsupported host features.

The included skills have names and descriptions; slash invocation is enabled by
default in hosts supporting this format. See
[VS Code skill documentation](https://code.visualstudio.com/docs/agent-customization/agent-skills)
and [customization guidance](docs/agents/customizations.md).

## Publish the starter on GitHub

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
       power-platform-onboarding/
         SKILL.md
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

## Configure platform tools separately

Copying these files does not install Power Platform CLI, Matt Pocock plugins,
Canvas Authoring MCP, Power Automate tooling, connectors, or licenses. It also
does not sign in to a tenant or create an app/solution.

During onboarding, identify only the tools needed for the planned work and follow
their current official setup instructions. Obtain required installation,
connection, and resource approvals. Authenticate through approved sign-in flows;
never put credentials in the registry or chat. Verify the actual account, tenant,
environment, and resource before writes.

## Included specialist customizations

The starter includes onboarding and architecture skills and an expert agent under
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
