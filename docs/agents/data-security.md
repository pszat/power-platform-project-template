# Data, storage, and security standard

## Model and persistence

Inspect existing tables, columns, relationships, constraints, access rules, and
consumers before designing changes. Reuse an existing model only when its business
meaning fits. Follow approved naming and publisher settings; request missing rules.

For schema changes, describe exact elements, purpose, data/dependency impact,
security implications, and test evidence. Obtain approval for the exact change.
Schema approval does not authorize migration, deletion, or other destructive work.

Store business data and files only in project-approved persistent stores.
Collections and variables may hold UI state/working copies, not the persistent
source of truth. Flow run history is diagnostic history, not a business register.
Do not bypass a model limitation by silently adding another persistent store.

Identify the source of truth, save boundary, validation, failure/recovery behavior,
concurrent update policy, and lifecycle requirements for affected data. Account for
expected query volume and performance.

## Files

Confirm the approved provider, site/container/library, identifiers, record linkage,
permissions, lifecycle, and recovery from partial operations. A Dataverse record
and a file operation are not automatically a single transaction.

For SharePoint, explicitly verify the relationship between Dataverse access and
site/library/file access. Do not assume that one grants or revokes the other.

## Access and sensitive information

- Use least privilege and verify data/service authorization, not only hidden UI.
- Establish caller, owner, team/role, and connection identities relevant to each
  operation; validate allowed and denied scenarios.
- Use synthetic/non-production examples. Do not place production data or
  confidential payloads into tests, screenshots, logs, or prompts.
- Keep passwords, tokens, cookies, client secrets, private keys, and recovery
  codes out of repositories, documentation, examples, and chat.
- Ordinary text environment variables are not a secret store. Use an approved
  secret-management/authentication mechanism; record references, not values.
- Account IDs, tenant URLs, resource IDs, and usernames may be sensitive metadata.
  Record only what client policy permits; use role aliases/secure lookup otherwise.
- Limit diagnostic fields and retention to approved needs. Sanitize errors and
  flow run visibility without silently swallowing operational failures.
- Before a new integration, verify available licensing, DLP, client restrictions,
  and required permissions. Request confirmation where evidence is unavailable.

Unknown security constraints block affected access or implementation; they are
not permission to choose a convenient default.
