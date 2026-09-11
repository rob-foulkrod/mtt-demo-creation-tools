---
version: 2026.09.11.1
name: demo-on-demand
description: |
  Builds public-safe demo-on-demand packages for MTT private deliveries and first asks, "Will you
  be uploading to GitHub?" Routes Yes to a GitHub-ready repository package and No to a
  Cowork-compatible overview Page plus `demo/` folder. Use when the user asks to "create a demo on
  demand", "build an MTT demo package", "make a Scout, Cowork, Copilot, Agent Builder, SharePoint
  agent, or Copilot Studio demo", "prepare a public GitHub demo repo", or "create demo artifacts
  for a private delivery". Do NOT use for confidential customer data or an MTT idea or initiative.
  Do NOT use for a standalone document - use docx instead; a standalone spreadsheet - use xlsx
  instead; or a deck or slide - use pptx instead.
---

Use this skill when an MTT wants to create a demo-on-demand package for a private delivery. The package must be generated from the user's current requirements and must not copy proprietary or copyrighted material from prior examples.

Skill version:
Version: 2026.09.11.1

Source references:
- Public repository: `https://github.com/rob-foulkrod/mtt-demo-creation-tools`
- Scout skill folder: `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/scout`
- Scout source file: `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/scout/demo-on-demand-SKILL.md`
- Cowork format reference: `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/cowork/demo-builder-SKILL.md`
- Generate-data skill folder: `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data`
- Generate-data source file: `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`
- Change logs folder: `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/change%20logs`

At the start of each use, check the Scout source file URL above when internet access is available. If the public GitHub copy has a higher version number than this local skill file, tell the user that a newer Scout version is available and prompt them to install it before continuing. If the user approves, download the updated Scout source file from the public GitHub URL, update the local skill, then reload the updated skill instructions before continuing. If the user declines, continue with the local skill and mention that they are using an older version. If the version cannot be checked, continue with the local skill and mention that the version check could not be completed.

Generate-data dependency:
- Required version: `2026.09.04.4` or newer.
- Before creating any fictional company, person, email address, or sample data, load the generate-data skill from `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data`.
- If the generate-data skill or its `companies.csv` and `names.csv` support files are not installed locally with this skill, offer to download and install the full folder from `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data` before generating data.
- When downloading directly, use the raw files from `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`, `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/companies.csv`, and `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/names.csv`.

Local file validation:
- Scout skill local path: `C:\Users\anconnif\.scout\m-skills\demo-on-demand\SKILL.md`.
- Generate-data local folder: `C:\Users\anconnif\.scout\m-skills\generate-data`.
- Before running, validate that the Scout skill local path exists and that the generate-data folder contains `SKILL.md`, `companies.csv`, and `names.csv`.
- If any required local file is missing, offer to download and install it from the full public GitHub URL listed above before continuing.
- If the user provides a different local Scout skills root, validate that path instead and report the exact path used.

Change log requirement:
- Every update to this skill must write a change log file in `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/change%20logs`.
- The change log file name must be `<skill-name>-<skill-version>-log.md`; for this skill, use `demo-on-demand-2026.09.11.1-log.md` for version `2026.09.11.1`.
- The change log title must be `<skill-name> <skill-version>-log`.
- The change log must include `Skill name`, `Skill version`, `Additions`, and `Deletions` sections. If there are no deletions, write `None`.
- Commit the change log file in the same commit as the skill update.

Core purpose:
Create a complete, public-safe demo package containing presenter instructions and supporting files for Microsoft technology demos tailored to an industry, role, fictional customer scenario, and realistic business workflow. The workflow must branch based on whether the user wants a public GitHub upload.

## Shared Core Contract

The scenario design, artifact quality, presenter-guide rules, public-safety requirements, and
verification standards in this skill intentionally match the Cowork demo builder. Keep those
shared rules synchronized when either skill changes. Publishing remains platform-specific:

- Scout asks whether the user will upload to GitHub and supports both the GitHub-ready and
  Cowork-compatible branches defined below.
- Cowork remains OneDrive/SharePoint-only and must not inherit Scout's GitHub question,
  repository files, licensing, GitHub CLI steps, or repository deletion workflow.

Apply these production-realistic artifact rules to both Scout branches:

1. **Research the real data shape first.** Research public, non-confidential examples,
  glossaries, workflows, forms, and industry conventions before creating scenario documents or
  datasets. Use that research to determine fields, identifiers, relationships, units, statuses,
  calculations, and record density. Synthesize original content rather than copying an example.
2. **Create one shared style system.** Define the package font, color palette, title treatment,
  heading hierarchy, table style, header band, row banding, border treatment, column widths,
  number formats, and date formats before building the first artifact. Apply that design language
  to every related Word, Excel, PowerPoint, PDF, Markdown, and visual artifact.
3. **Style every worksheet and document.** Every Excel sheet needs a meaningful title, filled
  header band, consistent font and palette, readable column widths, frozen headers, appropriate
  number formats, and charts or summaries when they support the scenario. Verify related files
  side by side before publishing.
4. **Use the scenario's locale.** Research or confirm the country and use its currency symbol,
  date format, decimal and thousands separators, address structure, phone pattern, and units.
  Store currency and dates as typed values with display formats when the file format supports it.
5. **Generate natural, invented identities.** Use realistic, made-up names and stable IDs for
  recurring people, organizations, products, projects, and locations. Avoid generic labels such
  as `Fictional Customer 0001`, `Sample Agency`, `Test Vendor`, or `Demo Company`.
6. **Identify source organizations like real sources.** Include both a stable source ID and a
  natural invented name for agencies, branches, vendors, hospitals, stores, partners, or other
  source organizations.
7. **Keep implementation details out of business data.** Do not put workbook names, file names,
  folder paths, prompt labels, or generation notes into ordinary business-record columns unless
  public research confirms the real system stores that provenance.
8. **Keep the scenario internally coherent.** Names, IDs, dates, amounts, products, statuses,
  locations, and relationships must agree across related files. Deliberate nonmatches are allowed
  only when they support a documented filtering, exception, quality, or validation step.
9. **Keep provenance language out of demonstration content.** Do not use `fictional`, `fake`,
  `synthetic`, `sample`, `test`, or `demo` in copy-and-paste prompts, business-record values,
  entity names, table titles, or ordinary scenario documents.
10. **Retain package-level transparency.** Put Public classification, AI transparency, the
   Microsoft Fake Company disclaimer, and the reminder not to add confidential information in
   the branch-specific overview files. Never represent invented records as actual records.

## When to Use

- "Create a demo on demand" or "build an MTT demo package."
- "Make a Scout, Cowork, Microsoft 365 Copilot, Agent Builder, SharePoint agent, or Copilot Studio demo."
- "Prepare a public GitHub demo repository."
- "Create a Cowork-compatible demo folder."
- "Build repeatable presenter instructions and supporting artifacts for a private delivery."

## When NOT to Use

- Confidential customer or tenant data, private URLs, credentials, or real customer-specific
  records.
- A standalone Word document -> use the **docx** skill.
- A standalone spreadsheet -> use the **xlsx** skill.
- A standalone slide deck -> use the **pptx** skill.
- An MTT idea or initiative -> use the **mtt-initiative-creator** skill.
- General GitHub repository work that is not an MTT demo-on-demand package.

Required first prompt:
Before collecting GitHub account, repository name, staging location, or destination folder, ask exactly: "Will you be uploading to GitHub?" Provide Yes and No choices. If the user already clearly answered Yes or No in the current request, record that answer and do not repeat the question.

Branching rules:
- If the user answers Yes, follow the GitHub-ready repository workflow. Require GitHub owner/account or organization and exact repository name. Build a public GitHub-ready package, preserve all download links, include demo instructions in both Markdown and Word, and use the shared `demo/` folder structure so all demo artifacts live under `demo/sample-data/`.
- If the user answers No, do not ask for GitHub account, organization, or repository name. Use the Cowork-compatible package workflow and file format: one scenario-named `.page` at the package root, one `demo/` folder, `demo/DEMO-INSTRUCTIONS.docx`, and `demo/sample-data/` containing every sample, grounding, imported, attached, opened, media, configuration, or supporting artifact. Do not create README.md, Markdown files, manifest files, `.github/`, LICENSE, GitHub repository scaffolding, or repository metadata unless the user later explicitly changes the answer to Yes.

Required intake workflow:
1. Ask: "Will you be uploading to GitHub?" with Yes/No choices unless the user already clearly answered it in the current request. Never re-ask an answered branch question.
2. Ask for the target industry, business scenario, and primary role or persona the demo should serve.
3. Ask whether they have a public customer web page, company web page, industry page, or role description to use as inspiration. Make clear this is optional and will only be used to infer public, non-confidential themes; the final demo must use a fictional Microsoft Fake Company, not the real customer name or data.
4. Prompt the user to choose the demo technology focus from these options, allowing combinations when appropriate: Microsoft 365 Copilot, Copilot prebuilt agents, Cowork, Microsoft Scout, a Custom Agent in Microsoft 365 Agent Builder, a SharePoint agent, Agent Builder in Chat, or Copilot Studio.
5. Ask for starting experience and build/use scope: for example Microsoft 365 Copilot Chat, Copilot Studio, SharePoint agent, Agent Builder, Scout, Cowork, or another exact app/agent experience; and whether the demo builds/configures something, uses an existing experience, or both.
6. Ask for any delivery-specific constraints, persona names, demo length, target audience, required files, required document types, must-show outcomes, or source websites if not already provided.
7. If GitHub upload is Yes, ask for the user's GitHub account or organization, the exact repository name, and whether a local OneDrive staging folder should be created before upload. Tell the user the repository will be created as public and that every generated artifact must be labeled Public before upload.
8. If GitHub upload is No, ask for the destination folder for the Cowork-compatible package and the scenario/package name. If no destination is provided, propose a sensible local or OneDrive staging folder and confirm it.
9. If the prompt is too thin to create a rich demo experience, ask for more detail. If the user has no additional detail, proactively search the web for public, non-confidential information about the industry, role, and broadly comparable company patterns, then use only public and generic insights.

Scenario sufficiency gate:
Before generating files, confirm there is enough information to define:
1. Business task or problem.
2. Persona.
3. Desired outcome or handoff.
4. Input or source type.
5. Decision, filter, calculation, transformation, or interaction to perform.
6. Expected output and at least one must-show success condition.
If two or more are missing, or the request is only a broad label, ask one focused question for the
missing details. If the user has no more detail, research public patterns and document clearly
labeled synthetic assumptions in the branch-specific overview. Technology, starting experience,
build/use scope, and destination must still be resolved.

Research and scenario-building workflow:
1. Always research or look up the target industry, role or persona, and company context before generating artifacts. Prefer sources the user provides; otherwise use public web sources for industry norms, vocabulary, business workflows, KPIs, regulatory context, and role responsibilities.
2. When the user provides a real company, use it only for public inspiration. The package must use a fictional Microsoft Fake Company with synthetic data and must not use real company names in sample records, screenshots, prompts, internal process names, financials, employee names, customer names, or metrics.
3. Create a concrete end-to-end workflow for the demo showing multiple inputs, handoffs, decisions, and outputs.
4. Prefer multi-artifact experiences. Use more than one document, spreadsheet, data file, prompt set, or configuration file when that better demonstrates how Copilot or an agent reasons across multiple inputs.
5. Record public source URLs and assumptions. For GitHub packages, cite them in README.md and
  manifest.json. For non-GitHub packages, cite them on the overview `.page`. Keep package context
  out of the concise presenter guide.
6. If public web research is unavailable or blocked, continue with clearly identified synthetic assumptions and document them in the appropriate overview and instructions files.

Public-data and privacy rules:
1. Never use confidential customer data, private tenant details, internal URLs, real people, or real customer-specific metrics.
2. If a real customer web page is provided, use it only as public inspiration for industry vocabulary, business priorities, and plausible use cases.
3. Replace the customer with a fictional Microsoft Fake Company. The fictional company name must be clearly artificial and must not imply endorsement by or affiliation with any real organization.
4. Include this disclaimer prominently in README.md for GitHub packages and on the overview
  `.page` for non-GitHub packages: "This demo uses a fictional Microsoft Fake Company created for
  demonstration purposes. Any resemblance to real organizations, people, products, services, or
  data is coincidental. Do not use customer confidential information in this demo package."
5. Label the package and generated artifacts Public where the format supports metadata or an
  unobtrusive footer. Include `Classification: Public` in README.md,
  AI-CONTENT-DECLARATION.md, the overview `.page`, and Office document properties or footers.
  Do not add classification text as an ordinary CSV/JSON record or business-data field. For
  binary or media artifacts, mark classification in the branch-specific overview or manifest.
6. Before creating a public repository or uploading anything visible to others, show the user a concise preview of generated contents and the exact public classification/disclaimer approach. Require explicit approval before public upload.

GitHub-ready output structure when GitHub upload is Yes:
Create a local repository folder named after the requested repository with this clean structure by default:
- README.md
- LICENSE
- AI-CONTENT-DECLARATION.md
- manifest.json
- demo/
- demo/DEMO-INSTRUCTIONS.md
- demo/DEMO-INSTRUCTIONS.docx
- demo/sample-data/

GitHub structure rules:
1. Keep all demo artifacts, including Word documents, Excel workbooks, CSV files, JSON files, images, media, grounding content, product configuration files, setup notes, persona cards, diagrams, and expected-result artifacts inside `demo/sample-data/`.
2. Keep presenter instructions in both `demo/DEMO-INSTRUCTIONS.md` and `demo/DEMO-INSTRUCTIONS.docx`. The two files must contain the same human-readable demo instructions.
3. Do not create top-level `artifacts/`, `sample-data/`, `setup/`, `media/`, `screenshots/`, or `prompts/` folders by default. If a product requires machine-readable configuration or media, place it under `demo/sample-data/` using clear subfolders only when helpful.
4. Preserve all download links. README.md and both demo instruction files must link to every file under `demo/sample-data/`. Before upload, use relative links. After GitHub upload, update links to GitHub blob or raw URLs consistently.
5. Include GitHub-only governance files only when appropriate, such as `.github/` issue or pull request templates, but never place demo artifacts outside `demo/sample-data/`.

Cowork-compatible output structure when GitHub upload is No:
Create a package folder named after the scenario with exactly this shape by default:
- <Scenario Name>.page
- demo/
- demo/DEMO-INSTRUCTIONS.docx
- demo/sample-data/

Cowork-compatible structure rules:
1. The package root contains one scenario-named `.page` and one `demo/` folder.
2. `demo/` contains only `DEMO-INSTRUCTIONS.docx` and `sample-data/`.
3. Store every file used, attached, grounded, imported, opened, configured, or referenced during the demo under `demo/sample-data/`.
4. Do not create README.md, DEMO-INSTRUCTIONS.md, AI-CONTENT-DECLARATION.md, LICENSE, manifest.json, `.github/`, repository metadata files, or separate markdown prompt files.
5. The `sample-data/` folder must not be empty. At minimum include a detailed business document or grounding file, a primary structured-data artifact, and an output template or expected-result artifact when applicable.
6. Record actual returned links only; do not invent SharePoint, OneDrive, or file links.
7. If the `.page` pipeline is unavailable, do not silently substitute Markdown or HTML. Report the unavailable Page as a blocker, continue building the approved `demo/` folder when useful, and do not describe the package as complete.

Required README.md content for GitHub packages:
1. Title and fictional Microsoft Fake Company name.
2. Classification: Public.
3. Fictional-company disclaimer.
4. Scenario overview, target industry, target role or persona, and public research basis.
5. Technology focus and prerequisites.
6. Repository contents table.
7. Demo workflow summary showing inputs, actions, outputs, and handoffs.
8. Download links for every supporting artifact under `demo/sample-data/`, plus links to `demo/DEMO-INSTRUCTIONS.md`, `demo/DEMO-INSTRUCTIONS.docx`, manifest, license, and AI-CONTENT-DECLARATION.md. Before upload, use relative links. After GitHub upload, update links to GitHub URLs.
9. Setup instructions.
10. MIT license notice.
11. AI transparency summary with a link to AI-CONTENT-DECLARATION.md.

Required overview `.page` content for non-GitHub packages:
1. Scenario title.
2. Fictional Microsoft Fake Company.
3. Classification: Public.
4. Fictional-company disclaimer.
5. Demo description.
6. Technology focus and exact starting experience.
7. Build/use scope.
8. Persona.
9. Audience.
10. Duration.
11. Prerequisites.
12. A short contents section linking to `demo/DEMO-INSTRUCTIONS.docx` and `demo/sample-data/`.
13. Public research sources.
14. Assumptions.
15. AI transparency notice.

Required DEMO-INSTRUCTIONS content:
For GitHub packages, create both `demo/DEMO-INSTRUCTIONS.md` and `demo/DEMO-INSTRUCTIONS.docx`. For non-GitHub packages, create only `demo/DEMO-INSTRUCTIONS.docx`.

The presenter guide should normally be one or two pages and use this clean structure:
1. Demo title.
2. Scenario: concise paragraph describing the task and desired outcome.
3. Demo Tool: exact app, exact agent or experience, and whether this is build, use, or both.
4. Files to Attach: bulleted list of files in execution order, all located under `demo/sample-data/`.
5. Prompts: numbered prompt headings in execution order. Put each exact copy-and-paste prompt in a
  shaded, bordered, single-cell prompt box. Each prompt must identify the files or knowledge
  sources in use, required result format, validation or acceptance criteria, failure or no-match
  behavior where relevant, and next handoff.
6. Build or Configure: include only when the demonstration creates or configures an agent. Name
  the exact interface, grounding files, instructions, starter prompts, tests, and handoff to Chat.
7. Test and Validate: include when the product must be built, published, permission-tested, or
  connected before it can be demonstrated.

Use-only demonstrations should remain one or two pages. Build-heavy SharePoint agent, Agent
Builder, and Copilot Studio guides may exceed two pages only for required current-interface setup,
permission checks, test prompts, expected results, and acceptance criteria. Do not add a cover
page, table of contents, executive summary, package inventory, long talk track, timing table,
cleanup section, troubleshooting section, repeated disclaimer, or overview material unless the
user explicitly requests it.

For Word, use a clean printable white page, one restrained blue accent, one professional sans-serif
font, real Heading 1 and Heading 2 styles, generous whitespace, short paragraphs, and simple file
bullets. Use a light single-cell callout table with a subtle border for each prompt. Avoid
decorative banners, crowded tables, excessive shading, and unnecessary headers. Put
`Classification: Public` unobtrusively in the footer or document properties. Validate the document
and visually inspect every rendered page before publishing.

GitHub `DEMO-INSTRUCTIONS.md` and `DEMO-INSTRUCTIONS.docx` must also include readable download links or file references for every supporting file. In Word, use readable hyperlinks or path references.

Required AI-CONTENT-DECLARATION.md content for GitHub packages:
1. Classification: Public.
2. Statement that the repository contains AI-generated and human-reviewed demo content.
3. Confirmation that all sample data, personas, company names, metrics, and documents are fictional unless explicitly identified as public source references.
4. Summary of public sources used, if any.
5. Reminder not to add customer confidential information to the repository.

Rich artifact requirements:
Every package must contain substantive, runnable, scenario-specific supporting artifacts. Unless a
format is genuinely inapplicable, include at least one detailed business document or grounding
file, one primary structured-data artifact, and one output template, destination file, or
expected-result artifact when the workflow creates a deliverable. Explain equivalent alternatives
in the branch-specific overview.

1. Word documents must be polished business artifacts rather than placeholders. SOPs, playbooks,
  and procedural guides must be several pages long and cover purpose, scope, roles,
  prerequisites, procedures, decisions, exceptions, controls, validation, troubleshooting, and
  expected outcomes.
2. Every primary Excel data workbook must contain at least 1,000 realistic data rows and more than
  one worksheet in both publishing branches. Include researched fields, stable entity and source
  IDs, natural invented names, lookup tabs, calculations, summaries, and charts where useful.
3. At least 50% of each primary source dataset must match the intended criteria. Include plausible
  nonmatches so the presenter must filter and reason over the data. Record and verify matching and
  nonmatching counts.
4. Use live Excel formulas for derived totals and verify that formulas calculate without errors.
5. CSV and JSON files must contain enough records for meaningful filtering, summarization, or
  grounding. Tiny illustrative datasets are insufficient.
6. Include visuals only when they materially support a demo step.
7. Every artifact must serve an input, action, decision, handoff, or output. Do not add filler.
8. For every major step, define the exact input, action or prompt, expected result, pass criteria,
  failure or no-match behavior, and next handoff.

Technology guidance:
1. **Microsoft 365 Copilot Chat:** Name the exact attached agent or experience, such as Excel,
  Researcher, an analysis agent, or a custom agent. Provide an end-to-end walkthrough with exact
  files, prompts, expected outputs, validation criteria, and handoffs.
2. **Copilot prebuilt agents:** Name the agent and provide access or setup assumptions, exact
  files, expected inputs, prompts, outputs, test cases, acceptance criteria, and next handoff.
3. **Cowork:** Name the exact starting surface and files. Include a complete walkthrough,
  collaboration steps, handoffs, expected outputs, safe artifacts, test prompts, acceptance
  criteria, and a clear private-delivery value story.
4. **Microsoft Scout:** Name the exact starting surface, source configuration, and files. Include a
  complete walkthrough, Scout-oriented prompts, collaboration or handoff steps, expected outputs,
  testable pass criteria, safe artifacts, and a value story comparable in depth to Cowork.
5. **SharePoint agent:** Include agent purpose, exact SharePoint grounding locations, detailed
  grounding files, instructions, starter prompts, access assumptions, setup, and later Chat use.
  Test grounded and cited answers, an out-of-scope or no-answer case, and a permission boundary.
6. **Agent Builder in Chat:** Use the current Agent Builder experience in Microsoft 365 Copilot
  Chat. Include purpose, instructions, grounding files, starter prompts, access assumptions, save
  or share steps, tests, expected results, acceptance criteria, and steps to select the agent.
7. **Copilot Studio:** Use only the new Copilot Studio interface. Do not include classic or
  legacy-interface directions. Include instructions, knowledge sources, trigger phrases, runnable
  actions or clearly labeled connector prerequisites, publish or channel steps, and later usage.
  Test a successful response, no-match or out-of-scope request, fallback behavior, and action
  failure. A connector placeholder is not a runnable demo step.

Licensing for GitHub packages:
Always create an MIT LICENSE file using the current year and the GitHub account or organization provided by the user as copyright holder unless the user specifies another public-safe copyright holder.

GitHub upload workflow when GitHub upload is Yes:
1. Do not create the public repository or upload artifacts until the user explicitly approves the generated artifacts and confirms they are public-safe.
2. Require both the user's GitHub account or organization and the exact repository name before upload.
3. Create a new public GitHub repository using the provided account or organization.
4. Prefer GitHub CLI if available and authenticated. Recommended command pattern: `gh repo create <owner>/<repo-name> --public --source . --remote origin --push` from inside the generated repository folder.
5. If the GitHub repository already exists, stop and ask the user whether to choose a different repository name or use the existing repository; do not overwrite an existing repository without explicit approval.
6. Upload all generated artifacts to the public repository in the first push.
7. After the first upload, update README.md, `demo/DEMO-INSTRUCTIONS.md`, and `demo/DEMO-INSTRUCTIONS.docx` so every supporting artifact has a GitHub download link.
8. Commit and push the link update after repository creation.
9. If GitHub CLI is not available or not authenticated, try standard git commands if a remote repository can be created or provided. If public repository creation is not possible in the current environment, leave a complete local repository and provide exact commands for the user to create the public repo and upload all artifacts.

Demo logging:
1. Do not log newly created demos to a shared catalog, SharePoint folder, workbook, list, or other tracking destination.
2. Demo logging is intentionally deferred until a future logging process is selected.
3. Use the public GitHub repository page `https://github.com/rob-foulkrod/mtt-demo-creation-tools` as the source for demo-builder skill updates and documentation.
4. After a GitHub demo package is published, report only the created repository URL and generated package contents. Do not create or update any separate catalog row.

Non-GitHub upload/verification workflow when GitHub upload is No:
1. Preview the package before writing or uploading: technology scope, starting experience, build/use scope, destination, root structure, sample-data contents, prompt sequence, sources, assumptions, and classification/disclaimer approach.
2. Require user approval before uploading to a shared SharePoint or OneDrive destination.
3. Create the package folder, overview `.page`, `demo/DEMO-INSTRUCTIONS.docx`, and all substantive sample artifacts under `demo/sample-data/`.
4. Upload or save files to the approved destination.
5. Verify final contents by re-listing the package structure and comparing against the expected checklist.
6. Report actual links returned by tools. Do not invent links.

Demo archive and deletion workflow:
1. If an MTT asks to delete, remove, retire, or archive a demo, first clarify whether they want to delete or archive the public GitHub repository, delete local generated files, remove generated destination files, or all of the above.
2. Never delete a public GitHub repository, local folder, or SharePoint file without explicit confirmation that names the target repository or file.
3. If the repository should remain but no longer be promoted, keep the repository and tell the user demo logging/catalog updates are not currently maintained by this skill.
4. If the repository should be deleted, confirm the exact `owner/repository` name, clearly state that repository deletion is irreversible, obtain explicit confirmation naming that target, and use GitHub CLI when authenticated.
5. If the local generated package folder should be deleted, confirm the exact local path before deleting it.
6. If a demo's own `manifest.json` is being updated during archive or deletion, set a repository-level status field when present or add one if needed, then commit and push that status update before any repository deletion.

Quality bar:
1. The package must be complete enough for an MTT to run the private delivery without asking for missing scripts or files.
2. Use clear, executive-friendly language and demo-step precision.
3. Keep fictional content realistic but not real-customer specific.
4. Confirm the GitHub upload branch before asking for GitHub account, organization, or repository name.
5. Validate that every generated file uses the correct branch-specific structure.
6. Validate that GitHub packages include README.md, LICENSE, AI-CONTENT-DECLARATION.md, manifest.json, `demo/DEMO-INSTRUCTIONS.md`, `demo/DEMO-INSTRUCTIONS.docx`, and all demo artifacts under `demo/sample-data/`.
7. Validate that non-GitHub packages contain one `.page`, one `demo/` folder, `demo/DEMO-INSTRUCTIONS.docx`, and non-empty `demo/sample-data/`, with no Markdown or repository files.
8. Validate that generated artifacts carry Public classification where appropriate and that the
  required disclaimer is present in the branch-specific README or overview Page without
  cluttering the presenter guide.
9. Validate that GitHub README.md, `demo/DEMO-INSTRUCTIONS.md`, and `demo/DEMO-INSTRUCTIONS.docx` include download links or readable file references for every supporting artifact after upload.
10. Validate that Word documents are substantive and a few pages long where Word documents are part of the demo.
11. Validate that every primary Excel workbook has multiple sheets, at least 1,000 rows, live
  error-free formulas where applicable, and verified matching and nonmatching counts with at
  least 50% matching the intended criteria.
12. Validate that prompts and human-readable instructions are consolidated in the branch-appropriate instruction files and prompt text is shown in clearly labeled boxes.
13. Validate that no separate demo catalog, SharePoint logging file, workbook, or list was created or updated.
14. Do not create or store secrets, credentials, tenant IDs, private URLs, or customer confidential content.
15. Validate that every related artifact follows the shared style system and scenario locale, uses
  stable IDs and natural invented names, and excludes implementation details from business data.

## Guardrails

- **Required branch question:** Always ask "Will you be uploading to GitHub?" before requesting
  GitHub details, a staging location, or a non-GitHub destination, unless the user has already
  clearly answered Yes or No in the current request. Never repeat an answered branch question.
- **Explicit scope confirmation:** Confirm the technology, starting experience, and whether the
  demonstration builds, configures, uses, or combines an agent or product experience.
- **Scenario sufficiency:** Do not generate files until the business task, persona, inputs,
  operation, expected output, and success conditions are defined or the user approves clearly
  labeled assumptions.
- **Public-safe content only:** Never use confidential customer data, real tenant details, private
  URLs, credentials, secrets, real people, or customer-specific metrics.
- **Never fabricate real facts:** Use researched public patterns and invented demo content. Do not
  present invented names, dates, figures, URLs, customer details, or product capabilities as real.
- **Approval before visible writes:** Preview the exact package, destination, classification, and
  disclaimer approach before creating a public repository or uploading to a shared folder.
- **No silent overwrite:** If a repository, package, or destination item already
  exists, identify it and obtain explicit direction before replacing or reusing it.
- **Destructive actions require named confirmation:** Never delete or permanently remove a
  repository, package, file, or folder without explicit confirmation naming the
  exact target. Prefer archive or retired status where possible.
- **Branch fidelity:** GitHub packages must contain the complete repository structure and download
  links. Non-GitHub packages must contain the overview Page and clean `demo/` structure without
  repository files.
- **Completion requires verification:** Re-list or inspect every final destination and do not
  report success while files, links, classifications, or required artifacts are
  missing.

When invoked, begin with the GitHub upload question unless the user already answered it in the current request. Ask only for missing fields after that branch is known. Research the industry, role, and company context; build a realistic multi-input workflow; generate the branch-appropriate local package; present a preview for approval; and then either publish to GitHub and report the created repository URL without logging it elsewhere, or save/upload the Cowork-compatible package and verify the final structure before reporting the workflow complete.
