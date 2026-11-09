# Workstation and authentication setup

This is a shared procedure template, not a credential repository.

## First use

1. Read the registry's approved account/tenant/environment selection. If missing,
   obtain the decision before connecting or writing.
2. Inspect available tools and their versions. Use supported setup documentation
   for missing prerequisites; obtain authorization for installations or connections.
3. Use the approved interactive or organization-managed authentication mechanism.
   The human completes sign-in/MFA where required. Never ask them to paste a
   password, token, cookie, client secret, or recovery code into chat.
4. Verify current account and tenant independently for Studio, CLI/Dataverse,
   flow tooling, and SharePoint where applicable. These may use different sessions.
5. Match actual target environment ID/URL to the approved registry entry. Verify
   app/solution/site context and permissions before affected writes.

Switching a browser profile or selecting a CLI auth profile can alter the target.
Inspect before changing state and reverify afterward. Do not copy credential
caches between accounts or commit exported authentication material.

## Machine-local notes

If needed, create `.local/setup.md` on the workstation, excluded by `.gitignore`.
It may contain:

- Local repository and working-app directory paths.
- Tool executable locations/versions.
- Non-secret auth-profile names and permitted browser-profile aliases.
- References to approved secure sign-in procedures.
- Last target verification date and outstanding setup issues.

It must not contain credentials. Ignored files can still leak through attachments,
backups, or diagnostics. If organizational policy restricts account metadata, keep
that metadata out as well and use approved role aliases.

Record portable verified facts in the shared registry only where policy permits.
This starter deliberately supplies neither a local setup file nor a live session.
