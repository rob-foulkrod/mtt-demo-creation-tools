# Cowork demo-builder presenter guide specification

Load this reference before creating `demo/DEMO-INSTRUCTIONS.docx`.

Use [the bundled Word guide](DEMO-INSTRUCTIONS-REFERENCE.docx) as the visual, structural, and
content-density reference. Match its cleanliness and hierarchy, but generate fresh
scenario-specific content. Do not copy its Pacific Northwest scenario text into unrelated demos.

## Default content structure

The guide should normally be one or two pages and contain only:

1. Demo title.
2. **Scenario** - one concise paragraph stating the task and desired outcome.
3. **Demo Tool** - the exact app and exact named agent or experience that must be selected or
   attached. State whether the presenter is building or using an agent.
4. **Files to Attach** - a short bulleted list of exact file names in the intended order. When files
   go to different experiences, state where each file is loaded, attached, grounded, imported, or
   opened.
5. **Prompts** - numbered prompt headings in execution order. Put each exact copy-and-paste prompt
   inside a shaded, bordered, single-cell prompt box. Each prompt must identify the files or
   knowledge sources in use, the required result format, the validation or acceptance criteria, and
   the next handoff. Keep these requirements inside the prompt so the guide remains clean.

Add a short **Build or Configure** section only when the demonstration creates or configures an
agent. Keep the setup steps separate from the later usage prompts and name the exact user interface,
grounding files, instructions, starter prompts, tests, and handoff to Chat. Add a short **Test and
Validate** section when the product must be built, published, permission-tested, or connected before
it can be demonstrated.

Use-only demonstrations should normally remain one or two pages. Build-heavy SharePoint agent,
Agent Builder, and Copilot Studio demonstrations may exceed two pages only when the additional space
contains required current-interface build steps, permission checks, test prompts, expected results,
and acceptance criteria. Preserve the same clean headings, short paragraphs, bullets, and prompt-box
treatment throughout.

Do not add a cover page, table of contents, executive summary, package inventory, long talk track,
timing table, cleanup section, troubleshooting section, repeated disclaimer, or explanatory material
that belongs on the overview Page unless the user explicitly requests it.

## Visual standard

- Use a clean, printable white page with one restrained blue accent.
- Use a single professional sans-serif font and a clear title.
- Use real Heading 1 and Heading 2 styles with generous whitespace.
- Keep paragraphs short and avoid dense prose.
- Present file names as simple bullets.
- Present every prompt in a light, single-cell callout table with a subtle border.
- Avoid decorative banners, crowded tables, excessive shading, and unnecessary headers.
- Put `Classification: Public` unobtrusively in the footer or document properties rather than
  repeating it throughout the body.
- Run document validation and visually inspect every rendered page before publishing.

## Clarity test

An MTT should be able to open the guide and immediately answer:

1. What scenario am I demonstrating?
2. Which product, app, or named agent do I select?
3. Which exact files do I load, and where?
4. Which prompts do I run, and in what order?
