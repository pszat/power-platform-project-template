# Canvas authoring standard

## Establish the supported editing path

Inspect the app, formulas, components, data sources, approved design, and available
authoring tools. Record the supported path in the registry before implementation.
Extracted `.pa.yaml` snapshots are not automatically editable application source;
verify how changes are applied to the actual app. Do not assume a retired
unpack/pack workflow or arbitrary YAML edits will round-trip.

If a Canvas Authoring coauthoring session is active, sync the app's working
directory before local edits. Use that session's supported editing and compilation
workflow, resolve introduced errors, and verify in Studio/runtime. Do not overwrite
newer maker edits. Without a supported path, stop affected edits and report the gap.

Approved reference YAML, working authoring files, solution source, and exports have
different roles. Keep the approved baseline immutable unless a baseline change is
authorized. Record how working edits are synchronized into source control.

## Design and dependencies

Follow the project's approved design workflow and
[asset index](../../references/canvas/README.md). Confirm controls, versions,
properties, components, theme, data sources, APIs, images, and formulas actually
exist. Query available tooling/reference definitions rather than inventing them.

An HTML mockup describes intended visuals, not equivalent executable Canvas
behavior. Surface material mapping limitations before implementation. Missing
approved references block the affected part; do not recreate approval from memory.

## Runtime quality

- Verify delegation for the actual query; prevent silently truncated results.
  Do not load entire tables into collections without a justified bounded case.
- Provide validation, explicit save/load/error states, and appropriate handling
  for duplicate clicks, partial failure, and concurrent editing.
- Keep temporary UI state distinct from persistent business data.
- Check references after renaming controls, screens, events, or navigation.
- Use the approved language and Power Fx syntax for the actual editor/tool.
  If the locale is unknown, state the separator convention.
- Test required window sizes, keyboard/accessibility behavior, and significant
  states according to approved device and accessibility requirements.
- UI visibility is not authorization; enforce access in the underlying service.

Use available compilation, App Checker, and accessibility checks where supported.
Report findings and limits explicitly. Functional verification and visual
verification are separate; an HTML preview or screenshot of a mockup proves
neither app behavior nor running-screen conformity.
