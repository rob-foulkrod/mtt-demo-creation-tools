---
version: 2026.09.04.2
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
Version: 2026.09.04.2

Source references:
- Public repository: `https://github.com/rob-foulkrod/mtt-demo-creation-tools`
- Scout skill folder: `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/scout`
- Scout source file: `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/scout/demo-on-demand-SKILL.md`
- Cowork format reference: `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/cowork/demo-builder-SKILL.md`
- Generate-data skill folder: `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data`
- Generate-data source file: `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`

At the start of each use, check the Scout source file URL above when internet access is available. If the public GitHub copy has a higher version number than this local skill file, tell the user that a newer Scout version is available and prompt them to install it before continuing. If the user approves, download the updated Scout source file from the public GitHub URL, update the local skill, then reload the updated skill instructions before continuing. If the user declines, continue with the local skill and mention that they are using an older version. If the version cannot be checked, continue with the local skill and mention that the version check could not be completed.

Generate-data dependency:
- Required version: `2026.09.04.2` or newer.
- Before creating any fictional company, person, email address, or sample data, load the generate-data skill from `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data`.
- If the generate-data skill or its `companies.csv` and `names.csv` support files are not installed locally with this skill, offer to download and install the full folder from `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data` before generating data.
- When downloading directly, use the raw files from `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`, `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/companies.csv`, and `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/names.csv`.

Local file validation:
- Scout skill local path: `C:\Users\anconnif\.scout\m-skills\demo-on-demand\SKILL.md`.
- Generate-data local folder: `C:\Users\anconnif\.scout\m-skills\generate-data`.
- Before running, validate that the Scout skill local path exists and that the generate-data folder contains `SKILL.md`, `companies.csv`, and `names.csv`.
- If any required local file is missing, offer to download and install it from the full public GitHub URL listed above before continuing.
- If the user provides a different local Scout skills root, validate that path instead and report the exact path used.

Core purpose:
Create a complete, public-safe demo package containing presenter instructions and supporting files for Microsoft technology demos tailored to an industry, role, fictional customer scenario, and realistic business workflow. The workflow must branch based on whether the user wants a public GitHub upload.

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
3. Desired outcome.
4. Input or source type.
5. Operation to perform.
6. Expected output.
7. Success conditions.
If any are missing, ask only for the missing details or propose reasonable synthetic assumptions for approval.

Research and scenario-building workflow:
1. Always research or look up the target industry, role or persona, and company context before generating artifacts. Prefer sources the user provides; otherwise use public web sources for industry norms, vocabulary, business workflows, KPIs, regulatory context, and role responsibilities.
2. When the user provides a real company, use it only for public inspiration. The package must use a fictional Microsoft Fake Company with synthetic data and must not use real company names in sample records, screenshots, prompts, internal process names, financials, employee names, customer names, or metrics.
3. Create a concrete end-to-end workflow for the demo showing multiple inputs, handoffs, decisions, and outputs.
4. Prefer multi-artifact experiences. Use more than one document, spreadsheet, data file, prompt set, or configuration file when that better demonstrates how Copilot or an agent reasons across multiple inputs.
5. Record public source URLs and assumptions. For GitHub packages, cite them in README.md, DEMO-INSTRUCTIONS.md, and manifest.json. For non-GitHub packages, cite them in the overview `.page` and DEMO-INSTRUCTIONS.docx.
6. If public web research is unavailable or blocked, continue with clearly identified synthetic assumptions and document them in the appropriate overview and instructions files.

Public-data and privacy rules:
1. Never use confidential customer data, private tenant details, internal URLs, real people, or real customer-specific metrics.
2. If a real customer web page is provided, use it only as public inspiration for industry vocabulary, business priorities, and plausible use cases.
3. Replace the customer with a fictional Microsoft Fake Company. The fictional company name must be clearly artificial and must not imply endorsement by or affiliation with any real organization.
4. Include this disclaimer prominently in README.md and DEMO-INSTRUCTIONS.md for GitHub packages, and in the overview `.page` and DEMO-INSTRUCTIONS.docx for non-GitHub packages: "This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package."
5. Label every generated artifact as Public where the format supports it. At minimum, include "Classification: Public" near the top of README.md, DEMO-INSTRUCTIONS.md, AI-CONTENT-DECLARATION.md, overview `.page`, generated supporting markdown, CSV, JSON, sample data, prompt, or configuration files. For binary or media artifacts, include a companion entry in the README/manifest or overview/instructions marking them Public.
6. Before creating a public repository or uploading anything visible to others, show the user a concise preview of generated contents and the exact public classification/disclaimer approach. Require explicit approval before public upload.

Always do:
1. Make every related generated file look like it belongs to the same professional package. Use consistent workbook themes, fonts, header styles, table styles, number formats, chart styling, terminology, and scenario naming across all related Excel, Word, Markdown, CSV, JSON, and supporting artifacts.
2. Always research what the target data should look like before generating sample records. Use realistic industry fields, identifiers, statuses, date ranges, units of measure, relationships, and data volumes for the selected scenario and country or region.
3. Format currencies, dates, percentages, phone numbers, postal codes, and measurements according to the scenario geography. Use `$` for US currency and the correct symbol or code for other countries or regions.
4. Always invent plausible company, agency, person, product, location, project, and record names. Avoid placeholder names, joke names, obvious test values, repeated names, or file names used as worksheet titles, data values, customer names, agency names, or business content.
5. Never label in-demo prompts, sample records, worksheet data, business documents, or generated operational artifacts as fictional, fake, synthetic, pretend, dummy, sample-only, or test data. Those safety concepts belong in public-safety disclaimers, AI transparency sections, README/overview materials, declarations, and manifest-style metadata only. The in-demo data itself should read like credible movie-prop business data while remaining entirely invented and public-safe.
6. When generating data from multiple pretend source systems, organizations, or agencies, include realistic source identifiers and display names. For insurance agency scenarios, include an Agency ID and an Agency Name column with credible invented agency names, and use those fields consistently across matching, reconciliation, and lookup artifacts.
7. Do not include silly or self-referential content such as worksheet rows named after the file, fields whose values are just the column name, obvious lorem ipsum, or labels that break the illusion of a real business workflow.

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
12. Contents links or file references to `demo/DEMO-INSTRUCTIONS.docx` and every file under `demo/sample-data/`.
13. Public research sources.
14. Assumptions.
15. AI transparency notice.

Required DEMO-INSTRUCTIONS content:
For GitHub packages, create both `demo/DEMO-INSTRUCTIONS.md` and `demo/DEMO-INSTRUCTIONS.docx`. For non-GitHub packages, create only `demo/DEMO-INSTRUCTIONS.docx`.

The presenter guide must use this clean structure:
1. Demo title.
2. Scenario: concise paragraph describing the task and desired outcome.
3. Demo Tool: exact app, exact agent or experience, and whether this is build, use, or both.
4. Files to Attach: bulleted list of files in execution order, all located under `demo/sample-data/`.
5. Prompts: numbered prompts. Each prompt must include exact prompt text, sources/files used, required result format, acceptance criteria, next handoff, failure behavior where relevant, and expected output.
6. Build or Configure, optional when the demo requires setup.
7. Test and Validate, optional but recommended for agent or workflow demos.
8. Cleanup steps where needed.

GitHub `DEMO-INSTRUCTIONS.md` and `DEMO-INSTRUCTIONS.docx` must also include readable download links or file references for every supporting file. In Word, use readable hyperlinks or path references.

Required AI-CONTENT-DECLARATION.md content for GitHub packages:
1. Classification: Public.
2. Statement that the repository contains AI-generated and human-reviewed demo content.
3. Confirmation that all sample data, personas, company names, metrics, and documents are fictional unless explicitly identified as public source references.
4. Summary of public sources used, if any.
5. Reminder not to add customer confidential information to the repository.

Rich artifact requirements:
1. Word documents must be substantive, polished business documents, not placeholders. A generated Word document should normally be a few pages long and include relevant headings, executive context, scenario details, tables or structured sections, and realistic fictional content.
2. Excel workbooks used as a primary dataset must include more than one worksheet. For GitHub packages, include at least 100 fictional data rows unless the scenario requires more. For non-GitHub/Cowork-compatible packages, target at least 1,000 rows for primary structured datasets, with calculations/formulas and lookup/reference tabs where useful.
3. CSV or JSON files must contain enough realistic synthetic records to support analysis, filtering, summarization, or agent grounding.
4. Include matching and nonmatching records, verified counts, and testability for major steps when the scenario depends on data matching, reconciliation, triage, or validation.
5. Include charts, diagrams, or visual summaries where useful. Place any exported images or media under `demo/sample-data/`.
6. Every artifact must serve the demo workflow. Do not add filler files solely to increase artifact count.

Technology guidance:
1. Microsoft 365 Copilot demos should focus on prompts, workflow orchestration, content generation, summarization, analysis, and meeting/email/document productivity across multiple rich inputs.
2. Copilot prebuilt agent demos should clearly identify which prebuilt agent is being demonstrated and provide realistic setup, usage instructions, expected inputs, and expected outputs.
3. Cowork demos should include collaboration workflow steps, prompts, expected handoffs, and how to show value in a private delivery.
4. Microsoft Scout demos should include Scout-oriented prompts, scenario walkthroughs, expected outputs, and safe sample artifacts.
5. M365 Agent Builder, Agent Builder in Chat, or SharePoint custom agent demos should include agent purpose, grounding files, instructions, starter prompts, test cases, acceptance criteria, and deployment/setup guidance.
6. Copilot Studio demos should include topic/agent design notes, sample trigger phrases, actions/connectors placeholders if needed, test scripts, fallback behavior, and sample data or documents that make the conversation realistic.

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

Demo catalog workflow for GitHub packages:
1. ALWAYS update the shared Demo-on-Demand catalog workbook after a demo repository is successfully published. This is mandatory for every published GitHub demo.
2. Use an Excel workbook, not a Word document, for the catalog because the catalog is a structured manifest that MTTs need to filter, sort, and maintain.
3. Default catalog location: the `Demos` folder in the same SharePoint site used by the MTT ideas and initiatives workflow, under `CA West Team IdeaHub`.
4. Default catalog file name: `Demo-on-Demand Catalog.xlsx`.
5. If the `Demos` folder or catalog workbook does not exist and permissions allow, create them. If direct SharePoint creation is not possible, create the workbook locally and provide the exact SharePoint destination for manual upload.
6. The catalog workbook must be labeled Public and include at least these columns: Demo name, Status, GitHub owner, GitHub repository, GitHub URL, Industry or scenario, Fictional Microsoft Fake Company, Technology focus, Target audience, Created date, Created by, Last updated date, Public classification confirmed, README URL, Demo instructions URL, Manifest URL, Notes.
7. Use `Active` for newly published demos unless the user specifies another status.
8. Add or update exactly one row per GitHub repository. If the repository already appears in the catalog, update the existing row instead of creating a duplicate.
9. Before uploading or replacing the shared catalog workbook, preview the row that will be added or changed and ask for user approval because the update is visible according to SharePoint permissions.
10. After updating the catalog, report the catalog location and row status.
11. If the catalog update cannot be completed because SharePoint, Excel, or permissions are unavailable, create a local catalog-update file containing the exact row values and provide the specific SharePoint catalog destination so the user can upload or apply it manually. Report this as a blocker, not as a successful catalog update.

Non-GitHub upload/verification workflow when GitHub upload is No:
1. Preview the package before writing or uploading: technology scope, starting experience, build/use scope, destination, root structure, sample-data contents, prompt sequence, sources, assumptions, and classification/disclaimer approach.
2. Require user approval before uploading to a shared SharePoint or OneDrive destination.
3. Create the package folder, overview `.page`, `demo/DEMO-INSTRUCTIONS.docx`, and all substantive sample artifacts under `demo/sample-data/`.
4. Upload or save files to the approved destination.
5. Verify final contents by re-listing the package structure and comparing against the expected checklist.
6. Report actual links returned by tools. Do not invent links.

Demo archive and deletion workflow:
1. If an MTT asks to delete, remove, retire, or archive a demo, first clarify whether they want to archive the catalog entry only, delete or archive the public GitHub repository, delete local generated files, remove generated SharePoint catalog entries, or all of the above.
2. Never delete a public GitHub repository, local folder, or SharePoint file without explicit confirmation that names the target repository or file.
3. Prefer archiving over deletion for the shared catalog. Set Status to `Archived` or `Deleted`, preserve the GitHub URL for traceability when appropriate, and add a note with the date and reason.
4. If the repository should remain but no longer be promoted, update the catalog row to `Archived` and do not delete the GitHub repository.
5. If the repository should be deleted, confirm the exact `owner/repository` name, clearly state that repository deletion is irreversible, obtain explicit confirmation naming that target, use GitHub CLI when authenticated, and then update the catalog row to `Deleted` with the deletion date and reason.
6. If the local generated package folder should be deleted, confirm the exact local path before deleting it.
7. If a demo's own `manifest.json` is being updated during archive or deletion, set a repository-level status field when present or add one if needed, then commit and push that status update before any repository deletion. If the repository is being deleted immediately, update only the shared catalog because the repository manifest will no longer be available.
8. After archive or deletion, validate that the shared catalog has no duplicate active rows for the demo.

Quality bar:
1. The package must be complete enough for an MTT to run the private delivery without asking for missing scripts or files.
2. Use clear, executive-friendly language and demo-step precision.
3. Keep fictional content realistic but not real-customer specific.
4. Confirm the GitHub upload branch before asking for GitHub account, organization, or repository name.
5. Validate that every generated file uses the correct branch-specific structure.
6. Validate that GitHub packages include README.md, LICENSE, AI-CONTENT-DECLARATION.md, manifest.json, `demo/DEMO-INSTRUCTIONS.md`, `demo/DEMO-INSTRUCTIONS.docx`, and all demo artifacts under `demo/sample-data/`.
7. Validate that non-GitHub packages contain one `.page`, one `demo/` folder, `demo/DEMO-INSTRUCTIONS.docx`, and non-empty `demo/sample-data/`, with no Markdown or repository files.
8. Validate that all generated files include Public classification where applicable and the required disclaimer is present in branch-appropriate overview and instruction files.
9. Validate that GitHub README.md, `demo/DEMO-INSTRUCTIONS.md`, and `demo/DEMO-INSTRUCTIONS.docx` include download links or readable file references for every supporting artifact after upload.
10. Validate that Word documents are substantive and a few pages long where Word documents are part of the demo.
11. Validate that Excel workbooks have multiple sheets and enough fictional data rows for the selected branch and scenario.
12. Validate that prompts and human-readable instructions are consolidated in the branch-appropriate instruction files and prompt text is shown in clearly labeled boxes.
13. Validate that the Demo-on-Demand catalog workbook was updated with exactly one Active row for published GitHub repositories, or that a catalog-update blocker and local catalog-update file were provided.
14. Do not create or store secrets, credentials, tenant IDs, private URLs, or customer confidential content.

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
  disclaimer approach before creating a public repository, uploading to a shared folder, or
  updating the shared demo catalog.
- **No silent overwrite:** If a repository, package, catalog row, or destination item already
  exists, identify it and obtain explicit direction before replacing or reusing it.
- **Destructive actions require named confirmation:** Never delete or permanently remove a
  repository, package, file, folder, or catalog entry without explicit confirmation naming the
  exact target. Prefer archive or retired status where possible.
- **Branch fidelity:** GitHub packages must contain the complete repository structure and download
  links. Non-GitHub packages must contain the overview Page and clean `demo/` structure without
  repository files.
- **Completion requires verification:** Re-list or inspect every final destination and do not
  report success while files, links, classifications, catalog updates, or required artifacts are
  missing.

When invoked, begin with the GitHub upload question unless the user already answered it in the current request. Ask only for missing fields after that branch is known. Research the industry, role, and company context; build a realistic multi-input workflow; generate the branch-appropriate local package; present a preview for approval; and then either publish to GitHub and update the shared catalog, or save/upload the Cowork-compatible package and verify the final structure before reporting the workflow complete.
