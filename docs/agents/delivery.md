# Analysis, delivery, and evidence

## Plan proportionally

Inspect current implementation and documentation first. Establish objective,
actors/access, main scenario and exceptions, inputs/outputs, business rules,
acceptance criteria, component impact, volumes, and performance needs in proportion
to the task. Reuse approved decisions rather than repeating discovery.

Distinguish approved decisions, proposals, assumptions, and facts needing
verification. Ask about ambiguous behavior and unapproved model, security,
integration/licensing, destructive, or design changes. Independent analysis may
continue while affected implementation waits.

Keep changes scoped; preserve unrelated user/maker work. Record exact approval in
the [approval log](../project/approvals.md), including limits and evidence.
A general request or mockup approval does not approve every dependent change.

## Source control and shared authoring

Agree the source/export method, source of truth, working locations, branch/PR rules,
commit authorization, and component ownership in the registry. Use a dedicated
unmanaged solution in DEV with the agreed publisher. Do not guess its identity.

Coordinate maker and agent editing: one writer per shared app/solution component
at a time unless the tooling and explicit partitioning safely support otherwise.
Worktrees do not isolate changes to the same live cloud app. Sync/inspect before
editing and review relevant diffs before exporting or committing.

Use `solutions/` only according to the verified tool layout. `working/` is ignored
temporary authoring state, not the durable deliverable. Ensure approved app changes
are saved in the platform and captured through the agreed durable source/export
workflow. Do not commit unrelated exports, generated noise, secrets, or data.

Follow project branch protection and review rules. Commit or push only when
authorized; approval to implement does not automatically authorize either.
Inspect staged changes and use available secret checks. Ignore patterns alone do
not protect credentials. No deployment pipeline is implied by these instructions.

## Documentation and tests

Update relevant documentation alongside implementation. New components and
significant changes need a purpose/dependency description and test scenarios.
Record meaningful architectural trade-offs as ADRs in `docs/decisions/`, including
status, context, alternatives, decision, and consequences.

Use root `GLOSSARY.md` for resolved business definitions, not implementation policy.
Create it only when needed. Use the actual configured tracker; do not invent issue
numbers, labels, or repositories.

Test observable acceptance criteria using available supported tools. Cover success,
validation, errors, permissions, and regression; include duplicates, concurrency,
and performance when relevant. Match effort to risk. Use test-first development
where practical at agreed seams, not fabricated unit-test tooling for Canvas.

Review the diff for project standards and requirement coverage. Record execution
command/tool, target, result, evidence, and limitations without sensitive payloads.

## Completion gates

1. Required approvals and target checks are satisfied.
2. Changes are applied through the supported workflow, saved, and durably captured.
3. Relevant available static/compile checks pass; unresolved findings are explicit.
4. Required runtime acceptance checks pass in the approved environment.
5. Visual verification, where applicable, inspects the running screen against the
   approved design and is reported independently of functional tests.
6. Documentation and change review are complete.

If access or tooling prevents a gate, report the exact blocker and status such as
`implemented; not runtime-verified`. Do not claim completion or silently substitute
a mockup, successful export, compilation, or local commit for runtime evidence.
List proposed follow-up tests separately from executed ones.

Final report: affected components, template/design version where relevant,
functional results, visual results, approval/deviation references, durable source
status, and remaining limitations/dependencies/open issues.
