---
version: 2.2.1
name: demo-on-demand
description: |
  Builds a clean, public-safe demo-on-demand package for an MTT private delivery and places it in
  a user-selected OneDrive or SharePoint folder. Produces one polished overview Page plus a
  `demo/` folder containing a concise Word presenter guide and substantive fictional sample data.
  Use when the user asks to "create a demo on demand", "build a demo package", "make a Copilot,
  Scout, Cowork, Agent Builder, SharePoint agent, or Copilot Studio demo", "create demo artifacts
  in a folder", or "prepare a private-delivery demo". Do NOT use for confidential customer data
  or a GitHub-ready repository. Do NOT use for document, docx, or Word-only deliverables - use docx
  instead. Do NOT use for a plain slide or deck - use the built-in pptx instead. Do
  NOT use for an MTT initiative.
cowork:
  category: automation
  icon: Rocket
---

## Version and Canonical Source

- **Current version:** `2.2.1`
- **Public repository:** `https://github.com/rob-foulkrod/mtt-demo-creation-tools`
- **Cowork skill folder:** `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/cowork`
- **Canonical source file:** `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/cowork/demo-builder-SKILL.md`
- **Generate-data skill folder:** `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data`
- **Generate-data source file:** `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`

Before running a demo-on-demand workflow, read the canonical source file from the public GitHub URL
above and compare its frontmatter `version` with this loaded copy. If the canonical version is
newer, use its current instructions for the run and tell the user that a newer version was found. Do
not overwrite the installed personal skill unless the user asks to update it. If the canonical file
cannot be accessed, continue with the loaded version and disclose the gap.

## Generate-data Dependency

- **Required version:** `2026.09.04.2` or newer.
- Load the generate-data skill before creating any fictional company, person, email address, or
  sample data.
- If the generate-data skill or its `companies.csv` and `names.csv` support files are not installed
  locally with this Cowork skill, offer to download and install the full folder from
  `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data` before
  generating data.
- When downloading directly, use the raw files from
  `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`,
  `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/companies.csv`,
  and
  `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/names.csv`.

## Local File Validation

- **Cowork skill local path:** `C:\Users\anconnif\.scout\m-skills\demo-on-demand\SKILL.md`.
- **Generate-data local folder:** `C:\Users\anconnif\.scout\m-skills\generate-data`.
- Before running, validate that the Cowork skill local path exists and that the generate-data folder
  contains `SKILL.md`, `companies.csv`, and `names.csv`.
- If any required local file is missing, offer to download and install it from the full public GitHub
  URL listed above before continuing.
- If the user provides a different local Cowork skills root, validate that path instead and report
  the exact path used.

When the user asks to update this skill:

1. Read the canonical source file before editing.
2. Increment the semantic version in both the frontmatter `version` field and the **Current
   version** line. Use a patch version for wording or fixes, a minor version for backward-compatible
   behavior additions, and a major version for incompatible workflow or output-structure changes.
3. Apply the change to the active personal skill when requested, then validate and score it.
4. Commit the identical validated `SKILL.md` content back to the public GitHub repository path
   `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/cowork`.
5. Read the saved canonical file again from
   `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/cowork/demo-builder-SKILL.md`
   and verify that its version and content match before reporting completion.

## Overview

Turn an MTT's private-delivery requirements into a polished, repeatable, public-safe demo stored
in the OneDrive or SharePoint folder the user chooses.

The output is intentionally folder-native rather than repository-shaped. Create one readable
overview Page at the package root and put the runnable demonstration inside a `demo/` folder.
Do not create Markdown documentation, a manifest, a README, GitHub files, or repository
scaffolding. Cowork packages are not prepared or posted as GitHub repositories.

Generate all content fresh from the user's requirements. Never copy proprietary or copyrighted
material from an example.

## ALWAYS Do - Production-Realistic Artifacts

Apply every rule in this section to every demo package.

1. **Research the real data shape first.** Before creating any scenario document or dataset,
   research public, non-confidential examples, glossaries, workflows, forms, and industry
   conventions to determine the fields, identifiers, relationships, units, statuses, calculations,
   and record density that the artifact should contain. Cite research sources on the overview Page
   and synthesize original content rather than copying an example.
2. **Create one shared style system for related files.** Before building the first artifact,
   define the package's font, color palette, title treatment, heading hierarchy, table style,
   header band, row banding, border treatment, column widths, number formats, and date formats.
   Apply that same design language to every related Word, Excel, PowerPoint, PDF, and visual
   artifact. Different files may vary in layout, but they must clearly look like parts of the same
   organization and workflow.
3. **Style every worksheet and document.** Never leave one workbook or secondary sheet with
   default formatting. Every Excel sheet needs a meaningful title, filled header band, consistent
   font and palette, readable column widths, frozen headers, appropriate number formats, and
   charts or summaries when they support the scenario. Verify related files side by side before
   uploading.
4. **Use the scenario's locale.** Research or confirm the country and use its currency symbol,
   date format, decimal and thousands separators, address structure, phone pattern, and units.
   Use `$` for United States currency, or the appropriate symbol for the confirmed country.
   Store currency and dates as real numeric or date values and apply display formats; never embed
   formatted money or dates as plain text when the file format supports typed values.
5. **Generate natural, invented identities.** Use realistic, made-up names for people,
   customers, agencies, vendors, products, projects, locations, and organizations. Give every
   recurring entity a stable ID and use that same ID and name consistently across related files.
   Avoid generic labels such as `Fictional Customer 0001`, `Sample Agency`, `Test Vendor`, or
   `Demo Company`.
6. **Identify pretend source organizations like real sources.** When records are supplied by
   agencies, branches, brokers, vendors, hospitals, stores, partners, or other source
   organizations, include both a stable source ID and a natural invented name, such as
   `Agency ID` and `Agency Name`. Use the equivalent business-appropriate fields for the
   scenario.
7. **Keep implementation details out of business data.** Do not put workbook names, file names,
   folder paths, prompt labels, or generation notes into ordinary business-record columns unless
   a researched real-world system would genuinely store that provenance. Distinguish sources with
   business identifiers and names rather than a `Source File` column.
8. **Keep the scenario internally coherent.** Names, IDs, dates, amounts, products, statuses,
   locations, and relationships must agree across every related file. Deliberate nonmatching or
   erroneous records are allowed only when they support a documented filtering, exception, data
   quality, or validation step.
9. **Keep provenance language out of the demonstration content.** Do not use the words
   `fictional`, `fake`, `synthetic`, `sample`, `test`, or `demo` in copy-and-paste prompts,
   business-record values, entity names, table titles, or ordinary scenario documents. Write from
   the perspective of the scenario's worker and organization.
10. **Retain package-level transparency.** The overview Page must still state that the package is
    AI-generated, human-review-ready demonstration content, include the Microsoft Fake Company
    disclaimer, and identify the package as Public. Production-realistic artifacts must never be
    represented as actual customer, employee, financial, clinical, or operational records.

## When to Use

- "Create a demo on demand" or "build a demo package."
- "Make an MTT private-delivery demo for this industry or role."
- "Build a Microsoft 365 Copilot, Scout, Cowork, Agent Builder, SharePoint agent, or Copilot
  Studio demo."
- "Create the demo artifacts and put them in this OneDrive or SharePoint folder."
- Any request for concise presenter instructions plus realistic fictional supporting assets.

## When NOT to Use

- Real customer names, tenant data, private URLs, confidential material, or customer-specific
  records. This skill creates fictional, Public-classified content only.
- A GitHub repository, README, source tree, or repo-ready demo package.
- A single narrative document -> use the **docx** skill.
- A standalone slide deck -> use the **pptx** skill.
- A spreadsheet without a broader demo package -> use the **xlsx** skill.
- An MTT idea or initiative -> use the **mtt-initiative-creator** skill.

## Example

**User:** "Build a Cowork demo on demand for a fictional energy procurement team and put it in my
Demo Deliveries SharePoint folder."

**Expected behavior:** Confirm the exact technology and starting experience, resolve the folder,
design a realistic multi-input workflow, create one overview Page, create a clean two-page Word
guide modeled on [the bundled reference](references/DEMO-INSTRUCTIONS-REFERENCE.docx), place every runnable artifact under
`demo/`, preview the structure, upload it after approval, and verify the final folder contents.

## Output Structure

Create exactly this package shape unless the user explicitly requests a different name:

```text
<Scenario Name>/
|-- <Scenario Name>.page
`-- demo/
    |-- DEMO-INSTRUCTIONS.docx
    `-- sample-data/
        |-- <every file used, attached, grounded, imported, or opened during the demo>
        `-- <optional product-required configuration or media files>
```

Rules:

1. The scenario-named `.page` is the only item at the package root other than `demo/`.
2. `demo/` contains only `DEMO-INSTRUCTIONS.docx` and `sample-data/`.
3. Put every supporting Word document, SOP, workbook, CSV, JSON import, image, grounding file,
   or other runnable demo asset inside `demo/sample-data/`.
4. Do not create `.md` or `.markdown` files anywhere in the package.
5. Do not create `manifest.json`, `README.md`, `AI-CONTENT-DECLARATION.md`, a separate setup
   guide, or a prompt-only file.
6. Do not create `.github/`, source-control files, repository metadata, or instructions for
   posting the package to GitHub.
7. Keep setup directions, file-loading instructions, and prompts in `DEMO-INSTRUCTIONS.docx`.
8. Keep package context, prerequisites, research sources, classification, disclaimer, and AI
   transparency on the overview Page.

## Workflow

### Phase 1 - Collect and confirm the scope

Use `core-AskUserQuestion` to collect missing information in as few cards as practical:

1. Target industry and business scenario.
2. Primary role or persona the demo should serve.
3. Optional public customer, company, industry, or role web page for inspiration. Explain that it
   will be used only for public themes and vocabulary; the demo will use a fictional Microsoft
   Fake Company.
4. Technology focus. Always confirm exactly which technology or technologies the package should
   demonstrate. Offer only relevant choices such as Microsoft 365 Copilot Chat, a named prebuilt
   agent, Cowork, Microsoft Scout, a SharePoint agent, Agent Builder in Chat, or Copilot Studio.
5. Starting experience. Always confirm whether the demonstration begins in Chat, Excel, a named
   agent, or an agent-building experience.
6. Agent scope. When an agent is involved, confirm whether the demo builds the agent, uses an
   existing agent, or does both. Confirm whether it is a SharePoint agent, Agent Builder agent,
   Copilot Studio agent, Scout, Cowork, or a named prebuilt agent.
7. Exact destination folder. Ask whether to use an existing OneDrive or SharePoint folder or
   create a new folder. Never assume the destination.
8. Delivery-specific requirements: audience, duration, persona names, required files, environment
   limits, source websites, and must-show outcomes.

If the conversation already supplies a field, do not ask for it again, except that technology,
starting experience, and build-versus-use scope must always be explicitly confirmed. Never create
versions for every supported product unless the user explicitly confirms that broad scope.

Before researching or creating files, apply a **scenario sufficiency gate**. The request has enough
scenario detail only when it identifies:

1. A concrete business task or problem.
2. The primary persona performing the task.
3. The intended business outcome or handoff.
4. At least one realistic input, source, or grounding-file type.
5. The decision, filter, calculation, transformation, or interaction the technology must perform.
6. The expected output and at least one must-show success condition.

If two or more of these are missing, or the scenario is only a broad label such as "HR onboarding,"
"procurement," or "a demo for my team," use `core-AskUserQuestion` once to request the missing
scenario details. Do not begin research, create artifacts, or create versions for multiple
technologies while the scenario remains light.

If the user has no additional scenario detail after that focused question, research public,
non-confidential patterns and clearly label the resulting workflow and artifact assumptions as
synthetic. Technology, starting experience, agent scope, and destination must still be resolved.

### Phase 2 - Resolve the destination and package root

1. Resolve the supplied folder with `sharepoint_onedrive-SearchDrive`,
   `sharepoint_onedrive-GetDriveChildren`, or the supplied folder link.
2. If several folders are equally plausible, use `core-AskUserQuestion` with the concrete matches.
3. When the user requested a new folder, create it with `sharepoint_onedrive-CreateFolder`.
4. Create one scenario-named package folder beneath the selected destination.
5. Plan an internal expected-file checklist. Do not publish that checklist as a manifest.
6. Record only folder and file links returned by tools. Never invent a link.

### Phase 3 - Research and design the scenario

1. Research the target industry, persona, and company context before generating artifacts. Prefer
   public sources supplied by the user; otherwise use public web sources for vocabulary, common
   workflows, KPIs, regulatory context, and role responsibilities.
2. Use a real company only as public inspiration. Replace it in all sample content with a clearly
   fictional Microsoft Fake Company.
3. Design a concrete end-to-end workflow with multiple inputs, decisions, handoffs, and outputs.
4. Choose only the files that serve the demonstrated workflow. More artifacts are not inherently
   better.
5. Record public sources and synthetic assumptions on the overview Page.
6. If research is unavailable, continue with clearly labeled synthetic assumptions.

### Phase 4 - Create the overview Page

Invoke the **create** skill and use its Page branch to create the single scenario overview Page.
Do not substitute Markdown or a README.

The Page must include:

1. Scenario title and fictional Microsoft Fake Company name.
2. `Classification: Public`.
3. This disclaimer:

   > This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any
   > resemblance to real organizations, people, products, services, or data is coincidental. Do
   > not use customer confidential information in this demo package.

4. A concise description of what the demo shows and the intended business outcome.
5. Confirmed technology, starting experience, and whether an agent is built, used, or both.
6. Primary persona, delivery audience, and suggested duration.
7. Prerequisites and environment assumptions.
8. A short contents section linking to `demo/DEMO-INSTRUCTIONS.docx` and `demo/sample-data/`.
9. Public research sources and clearly labeled synthetic assumptions.
10. AI transparency: the package contains AI-generated, human-review-ready fictional demo content.
11. A reminder not to add confidential customer information.

Keep the Page polished and concise. It replaces the previous overview, setup guide, manifest, and
AI declaration files.

If the Page pipeline cannot place the `.page` in the requested destination, do not silently create
Markdown or HTML instead. Publish the Page through the available Page pipeline, report its actual
location, and keep the `demo/` folder in the selected destination.

### Phase 5 - Create the clean Word presenter guide

Create `demo/DEMO-INSTRUCTIONS.docx` through the **docx** skill and artifact tools.

Use [the bundled Word guide](references/DEMO-INSTRUCTIONS-REFERENCE.docx) as the visual,
structural, and content-density reference. Match its cleanliness and hierarchy, but generate fresh
scenario-specific content.
Do not copy its Pacific Northwest scenario text into unrelated demos.

#### Default content structure

The guide should normally be one or two pages and contain only:

1. Demo title.
2. **Scenario** - one concise paragraph stating the task and desired outcome.
3. **Demo Tool** - the exact app and exact named agent or experience that must be selected or
   attached. State whether the presenter is building or using an agent.
4. **Files to Attach** - a short bulleted list of exact file names in the intended order. When
   files go to different experiences, state where each file is loaded, attached, grounded,
   imported, or opened.
5. **Prompts** - numbered prompt headings in execution order. Put each exact copy-and-paste prompt
   inside a shaded, bordered, single-cell prompt box. Each prompt must identify the files or
   knowledge sources in use, the required result format, the validation or acceptance criteria,
   and the next handoff. Keep these requirements inside the prompt so the guide remains clean.

Add a short **Build or Configure** section only when the demonstration creates or configures an
agent. Keep the setup steps separate from the later usage prompts and name the exact user
interface, grounding files, instructions, starter prompts, tests, and handoff to Chat. Add a short
**Test and Validate** section when the product must be built, published, permission-tested, or
connected before it can be demonstrated.

Use-only demonstrations should normally remain one or two pages. Build-heavy SharePoint agent,
Agent Builder, and Copilot Studio demonstrations may exceed two pages only when the additional
space contains required current-interface build steps, permission checks, test prompts, expected
results, and acceptance criteria. Preserve the same clean headings, short paragraphs, bullets, and
prompt-box treatment throughout.

Do not add a cover page, table of contents, executive summary, package inventory, long talk track,
timing table, cleanup section, troubleshooting section, repeated disclaimer, or explanatory
material that belongs on the overview Page unless the user explicitly requests it.

#### Visual standard

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

Clarity test: an MTT should be able to open the guide and immediately answer:

1. What scenario am I demonstrating?
2. Which product, app, or named agent do I select?
3. Which exact files do I load, and where?
4. Which prompts do I run, and in what order?

### Phase 6 - Create substantive sample data

Create every supporting artifact through the appropriate file skill and artifact tools. Put all
of them in `demo/sample-data/`.

Every demonstration must contain substantive, runnable, scenario-specific supporting artifacts.
An empty `sample-data/` folder, placeholder-only files, external links without local demo inputs,
or a guide that refers to files that were not created fails verification.

Unless the technology makes one format genuinely inapplicable, the default minimum is:

- At least one detailed scenario-specific business document or grounding file.
- At least one primary structured-data artifact used for filtering, calculation, analysis,
  retrieval, orchestration, or action testing.
- At least one output template, destination file, or expected-result artifact when the workflow
  updates or creates a business deliverable.

If a default artifact type is genuinely inapplicable, provide an equally substantive alternative
and explain the reason on the overview Page.

1. **Word documents:** Each scenario document must be a polished business artifact rather than a
   placeholder. SOPs, playbooks, and procedural guides must be several pages long and highly
   detailed, including purpose, scope, roles, prerequisites, procedures, decision points,
   exceptions, controls, validation, troubleshooting, and expected outcomes.
2. **Excel workbooks:** Every Excel data workbook must contain at least 1,000 realistic data rows
   and more than one worksheet. Include researched business-appropriate columns, stable entity and
   source IDs, natural invented names, reference or lookup tabs, calculations, summaries, and
   charts where useful. Related workbooks must share the same style system and field conventions.
3. **Data realism:** At least 50% of each primary source dataset must match the intended criteria.
   Include a meaningful number of plausible nonmatches such as other regions, dates, stages,
   categories, or conditions so the presenter must filter and reason over the data. Record and
   verify the matching and nonmatching counts for each primary dataset.
4. **Calculated values:** Use live Excel formulas for derived totals and verify that formulas
   calculate without errors.
5. **CSV and JSON:** Include enough synthetic records to support meaningful filtering,
   summarization, or agent grounding. Tiny illustrative datasets are not sufficient.
6. **Visuals and media:** Include them only when they materially support a demo step.
7. **No filler:** Every file must support a specific input, action, decision, handoff, or output.
8. **Public labeling:** Put `Classification: Public` in Office files and other assets where
   practical without making the presenter guide visually noisy.
9. **Testability:** For every major step, define the exact input, action or prompt, expected result,
   pass criteria, failure or no-match behavior, and next handoff.
10. **Business-facing language:** Remove generation commentary and provenance words from prompts,
    business records, source names, and ordinary artifact titles. Keep disclosure on the overview
    Page rather than repeating it inside the scenario.

### Phase 7 - Apply technology-specific guidance

- **Microsoft 365 Copilot Chat:** Name the exact attached agent or experience, such as Excel,
  Researcher, an analysis agent, or a custom agent. Provide an end-to-end walkthrough with the
  exact files attached at each step, prompts, expected outputs, validation criteria, and handoffs.
- **Copilot prebuilt agents:** Name the agent and provide access or setup assumptions, exact files,
  expected inputs, prompts, outputs, test cases, acceptance criteria, and the next handoff.
- **Cowork:** Name the exact starting surface and files. Include a complete scenario walkthrough,
  collaboration steps, handoffs, expected outputs, safe sample artifacts, test prompts, acceptance
  criteria, and a clear private-delivery value story.
- **Microsoft Scout:** Name the exact starting surface, source configuration, and files. Include a
  complete scenario walkthrough, Scout-oriented prompts, collaboration or handoff steps, expected
  outputs, testable pass criteria, safe sample artifacts, and a value story comparable in depth to
  Cowork.
- **SharePoint agent:** Include agent purpose, exact SharePoint grounding locations, detailed
  grounding files, instructions, starter prompts, access assumptions, setup, and later Chat usage.
  Test expected grounded and cited answers, an out-of-scope or no-answer case, and a permission
  boundary. Define the expected result and pass criteria for every test.
- **Agent Builder in Chat:** Use the current Agent Builder experience in Microsoft 365 Copilot
  Chat. Include agent purpose, instructions, grounding files, starter prompts, access assumptions,
  save or share steps, tests with expected results, acceptance criteria, and the exact steps to
  select or attach the finished agent.
- **Copilot Studio:** Use only the new Copilot Studio user interface. Do not include classic or
  legacy-interface directions. Include agent instructions, knowledge sources, trigger phrases,
  runnable actions or clearly labeled connector prerequisites, publish or channel steps, and later
  usage. Include test cases for a successful response, no-match or out-of-scope request, fallback
  behavior, and action failure, with expected results and pass criteria. A connector placeholder
  does not count as a runnable demo step.

### Phase 8 - Preview, approve, upload, and verify

Before uploading, show a concise preview containing:

1. Confirmed technology scope and starting experience.
2. Whether the demo builds an agent, uses one, or both.
3. Resolved destination and scenario package name.
4. The exact two-item root structure: the overview Page and `demo/`.
5. Every file that will appear under `demo/sample-data/`.
6. The exact tool or agent, files, and prompt sequence from `DEMO-INSTRUCTIONS.docx`.
7. Public classification, fictional-company disclaimer, research sources, and assumptions.

Require explicit user approval before uploading because the destination may be visible to others.

After approval:

1. Create the scenario package folder and `demo/sample-data/` with
   `sharepoint_onedrive-CreateFolder`.
2. Upload `DEMO-INSTRUCTIONS.docx` and every supporting artifact with
   `sharepoint_onedrive-UploadFileContent`.
3. Preserve the exact structure.
4. Re-list the package root, `demo/`, and `demo/sample-data/` with
   `sharepoint_onedrive-GetDriveChildren`.
5. Follow pagination until the complete contents are checked.
6. Compare the listing with the internal expected-file checklist and verify that no Markdown,
   manifest, README, or repository file exists.
7. If an upload fails, retry once. If anything is missing or extra, report the exact gap and do
   not describe the package as complete.
8. Report the actual Page and folder links returned by tools.

## Quality Bar

- The package root contains exactly one overview Page and one `demo/` folder.
- `demo/` contains only `DEMO-INSTRUCTIONS.docx` and `sample-data/`.
- No Markdown, manifest, README, repository metadata, or GitHub-posting guidance is generated.
- The Word presenter guide matches the reference guide's clean one-to-two-page design and contains
  only the scenario, exact demo tool or attached agent, exact files, and numbered prompt boxes,
  plus a concise build section when genuinely required.
- Every demo step names the exact file, where it is loaded, the selected app or agent, the prompt,
  expected result, pass criteria, failure behavior, and next handoff.
- Technology, starting experience, and build-versus-use scope are explicitly confirmed.
- Light scenarios trigger one focused question for the missing task, persona, inputs, business
  rules, expected output, and must-show success conditions before generation starts.
- `demo/sample-data/` is never empty and always contains substantive scenario-specific inputs plus
  an output or expected-result artifact when the workflow creates or updates a deliverable.
- Word scenario documents are substantive; detailed SOPs are several pages long.
- Every Excel data workbook has multiple sheets and at least 1,000 data rows.
- At least 50% of every primary source dataset matches the intended criteria, with verified counts
  and realistic nonmatching data.
- Every related artifact uses one documented style system, including consistent fonts, palette,
  headings, tables, number formats, currency, dates, and visual treatment.
- Data structures are based on public research and include realistic business fields, stable IDs,
  and natural invented names rather than generic generated labels.
- Source organizations are represented by business-appropriate ID and name fields. Workbook names,
  file paths, and generation notes do not appear as ordinary business data.
- Currency, dates, addresses, phone patterns, separators, and units match the confirmed country or
  locale.
- Copy-and-paste prompts and business-facing data do not call themselves fictional, fake,
  synthetic, sample, test, or demo; package-level transparency remains on the overview Page.
- Public classification and the Microsoft Fake Company disclaimer remain present without making
  the presenter guide cluttered.
- Every final artifact is verified, every rendered guide page is visually inspected, and every
  uploaded file is present before completion is reported.

## Guardrails

- **Fictional and Public only:** Refuse confidential, tenant-specific, or real-customer records.
- **Scope confirmation required:** Always confirm technology, starting experience, and whether an
  agent is built or used. Never create demos for every supported tool without explicit approval.
- **Scenario sufficiency required:** If the request lacks a concrete task, persona, inputs,
  business operation, expected output, or success condition, ask one focused question before
  research or creation.
- **Clean guide required:** Use the bundled reference and do not expand the Word guide into a
  handbook. Build-heavy guides may be longer only for required setup, permissions, tests, and
  acceptance criteria.
- **Page, not Markdown:** Never substitute a Markdown README for the overview Page.
- **No repository package:** Do not prepare, scaffold, or post the demo as a GitHub repository.
- **Destination required:** Resolve the exact OneDrive or SharePoint folder before uploading.
- **Approval before upload:** Preview the complete Page and folder structure, then obtain explicit
  approval before writing to the shared destination.
- **No secrets:** Never create or store credentials, tokens, tenant IDs, or private URLs.
- **No fabricated links:** Use only Page, folder, and file links returned by tools.
- **No placeholder deliverables:** Final artifacts must contain substantive demo content or
  transparently report the remaining gap.
- **No empty sample-data folder:** At least one substantive input or grounding artifact is always
  required, with an output or expected-result artifact when the workflow produces a deliverable.
- **No inconsistent styling:** Do not publish related files until every file and every sheet has
  been checked against the shared style system.
- **No generic generated identities:** Do not use numbered fictional-customer labels, `Sample`,
  `Test`, `Fake`, or `Demo` as business entity names.
- **No implementation columns:** Do not add file names, folder paths, prompt names, or authoring
  notes to business datasets unless public research confirms that the real system stores them.
- **Transparency stays outside the records:** Never remove the Public classification, AI
  transparency, or Microsoft Fake Company disclaimer from the overview Page, and never imply that
  invented records are real customer or operational data.
- **Verify every upload:** Re-list all three levels and compare them with the internal expected-file
  checklist before reporting success.
