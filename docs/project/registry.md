# Project registry: non-secret facts and readiness

Status: onboarding required. No cloud target is approved by this template.

Read [onboarding](../agents/onboarding.md) before populating this file. Store only
client-permitted metadata. Keep credentials out, including credentials embedded
in URLs. Use an approved role alias and secure reference when identities or
resource identifiers cannot be tracked.

## Status and evidence

For each populated group below, add source, checked date, and verifier. Use:

- `unknown`: not established.
- `proposed`: awaits decision; not approved.
- `pending creation`: authorized creation, resource does not yet exist.
- `verified`: inspected in the actual context, with evidence/date.
- `not applicable`: include a reason.

The identity authorized to connect is not necessarily the identity currently
connected. Record the approved selection here and reverify the active session
before writes. A registry entry is not an approval or proof of connection.

## 1. Purpose and ownership

| Field | Value |
|---|---|
| Project name and business objective | unknown |
| Business owner / technical owner / approver roles | unknown |
| Users, roles, main scenarios and exceptions | unknown |
| In-scope components and excluded work | unknown |
| Application language / documentation language | unknown |
| Browser, devices, window sizes, accessibility requirements | unknown |
| Expected data volumes, usage and performance targets | unknown |
| Data classification and permitted tracked metadata | unknown |
| Acceptance criteria and requirements reference | unknown |
| Evidence / checked date / verifier | unknown |

## 2. Repository and work tracking

| Field | Value |
|---|---|
| Repository URL / owner / visibility | unknown |
| Tracker and project/board reference | unknown |
| Default branch / branch and PR review rules | unknown |
| Commit / push authorization | unknown |
| Existing instruction entry point and agent host | unknown |
| Source-of-truth and supported export/import workflow | unknown |
| Shared component editing ownership / coordination | unknown |
| Tool names, verified versions, verification commands | unknown |
| Evidence / checked date / verifier | unknown |

## 3. Environment targets and approved identity selection

Create one row per environment; use no invented example identifiers.

| Target role | Environment ID | Dataverse URL | Tenant ID or secure reference | Approved account alias/role | Approved operations and evidence | Checked date |
|---|---|---|---|---|---|---|
| Development candidate, not yet approved | unknown | unknown | unknown | unknown | none recorded | unknown |

| Field | Value |
|---|---|
| How to verify current Studio user/tenant/environment | unknown |
| How to verify current CLI/Dataverse caller and target | unknown |
| Permission/role evidence for required actions | unknown |
| Whether non-DEV work is in scope | unknown; no non-DEV writes authorized |
| DLP/client restrictions and verification source/date | unknown |
| Licensing/capacity prerequisites and verification source/date | unknown |

## 4. Solution and publisher

| Field | Value |
|---|---|
| DEV solution display name / unique name / version | unknown |
| Confirmed unmanaged status / environment | unknown |
| Publisher name / unique name / customization prefix | unknown |
| Schema naming convention / approved exact names | unknown |
| Component dependencies and existing solution references | unknown |
| Supported unpacked source location / export procedure | unknown |
| Evidence / checked date / verifier | unknown |

## 5. Canvas app and Studio

Create a separate section per app where needed.

| Field | Value |
|---|---|
| App name / app ID / environment ID | unknown |
| Verified Studio edit link, without session credentials | unknown |
| Runtime link / app owner role / authoring access | unknown |
| Approved Studio account alias and tenant | unknown |
| Existing app versus approved new-app creation | unknown |
| Supported authoring method / tooling / limitations | unknown |
| Coauthoring connection and sync/compile procedure | unknown |
| Machine-local working path reference | unknown; actual path stays in .local/ |
| Agreed durable app source/export method and location | unknown |
| Data sources / components / APIs and dependencies | unknown |
| Formula locale / separators used by each editing surface | unknown |
| Approved template, control, theme and mockup asset IDs | unknown |
| Evidence / checked date / verifier | unknown |

## 6. Dataverse and security

| Field | Value |
|---|---|
| Table logical/schema names and relationship reference | unknown |
| Existing schema inspection source/date | unknown |
| Data ownership / roles / teams / access boundaries | unknown |
| Approved schema changes and approval references | none recorded |
| Required connector/API identities and permissions | unknown |
| Validation / duplicate keys / concurrent update policy | unknown |
| Synthetic test data setup / cleanup authorization | unknown |
| Retention, deletion, auditing and compliance requirements | unknown |
| Evidence / checked date / verifier | unknown |

## 7. Files and SharePoint, if selected

| Field | Value |
|---|---|
| Approved file provider and storage policy | unknown |
| Site URL/ID / library title and internal ID / folder rules | unknown |
| Record-to-file identifier/link mapping | unknown |
| Upload/download identity and effective permissions | unknown |
| Access alignment with Dataverse / external sharing | unknown |
| Size/type limits / retention / partial-failure recovery | unknown |
| Evidence / checked date / verifier | unknown |

## 8. Automation and connections

Repeat one row per flow and connection reference. Store identifiers and approved
identity aliases only, never credentials or connection payloads.

| Flow name / ID | Environment / solution | Trigger and side effects | Owner role / execution identity | Connections and references | State and approval evidence |
|---|---|---|---|---|---|
| unknown | unknown | unknown | unknown | unknown | not verified |

| Field | Value |
|---|---|
| Connection-reference logical names / connectors / approved owners | unknown |
| Run-only user and connection behavior, where relevant | unknown |
| Environment-variable schema names / purpose / secure value source | unknown |
| Retry / concurrency / idempotency / recovery decisions | unknown |
| Error monitoring, diagnostic access and sensitive-field handling | unknown |
| Approved validation, publish, enable and test-run operations | none recorded |
| Evidence / checked date / verifier | unknown |

## 9. Design and verification

| Field | Value |
|---|---|
| Design approval workflow and approver | unknown |
| Asset index and approved version references | see reference index; no assets supplied |
| Functional test procedure / target / evidence location | unknown |
| Visual test procedure / target sizes / evidence location | unknown |
| Permission, duplicate, concurrency and performance checks | unknown |
| Tooling/static checks and known limits | unknown |
| Definition of completion / review requirements | see delivery standard; project details unknown |
| Evidence / checked date / verifier | unknown |

## 10. Current readiness

| Work item / component | Verified prerequisites | Missing decisions or dependencies | Safe next action | Status / checked date |
|---|---|---|---|---|
| First-use setup | instruction templates only | actual project facts and approvals | read-only discovery and grouped intake | not implementation-ready |
