# Cowork demo-builder quality standards

Load this reference before creating demo artifacts, sample data, business documents, or validation
checks for the Cowork demo-builder skill.

## Production-realistic artifacts

Apply every rule in this section to every demo package.

1. **Research the real data shape first.** Before creating any scenario document or dataset,
   research public, non-confidential examples, glossaries, workflows, forms, and industry
   conventions to determine the fields, identifiers, relationships, units, statuses, calculations,
   and record density that the artifact should contain. Cite research sources on the overview Page
   and synthesize original content rather than copying an example.
2. **Create one shared style system for related files.** Before building the first artifact, load
   the bundled `demo-builder-style-guidelines` skill from the same release, then
   define the package's font, color palette, title treatment, heading hierarchy, table style,
   header band, row banding, border treatment, column widths, number formats, and date formats.
   Apply that same design language to every related Word, Excel, PowerPoint, PDF, and visual
   artifact. Different files may vary in layout, but they must clearly look like parts of the same
   organization and workflow.
3. **Style every worksheet and document.** Never leave one workbook or secondary sheet with
   default formatting. Every Excel sheet needs a meaningful title, filled header band, consistent
   font and palette, readable column widths, frozen headers, appropriate number formats, and charts
   or summaries when they support the scenario. Verify related files side by side before uploading.
4. **Use the scenario's locale.** Research or confirm the country and use its currency symbol, date
   format, decimal and thousands separators, address structure, phone pattern, and units. Use `$`
   for United States currency, or the appropriate symbol for the confirmed country. Store currency
   and dates as real numeric or date values and apply display formats; never embed formatted money
   or dates as plain text when the file format supports typed values.
5. **Generate natural, invented identities.** Use realistic, made-up names for people, customers,
   agencies, vendors, products, projects, locations, and organizations. Give every recurring entity
   a stable ID and use that same ID and name consistently across related files. Avoid generic labels
   such as `Fictional Customer 0001`, `Sample Agency`, `Test Vendor`, or `Demo Company`.
6. **Identify pretend source organizations like real sources.** When records are supplied by
   agencies, branches, brokers, vendors, hospitals, stores, partners, or other source organizations,
   include both a stable source ID and a natural invented name, such as `Agency ID` and `Agency
   Name`. Use the equivalent business-appropriate fields for the scenario.
7. **Keep implementation details out of business data.** Do not put workbook names, file names,
   folder paths, prompt labels, or generation notes into ordinary business-record columns unless a
   researched real-world system would genuinely store that provenance. Distinguish sources with
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

## Substantive sample data

Unless the technology makes one format genuinely inapplicable, the default minimum is:

- At least one detailed scenario-specific business document or grounding file.
- At least one primary structured-data artifact used for filtering, calculation, analysis,
  retrieval, orchestration, or action testing.
- At least one output template, destination file, or expected-result artifact when the workflow
  updates or creates a business deliverable.

If a default artifact type is genuinely inapplicable, provide an equally substantive alternative and
explain the reason on the overview Page.

1. **Word documents:** Each scenario document must be a polished business artifact rather than a
   placeholder. SOPs, playbooks, and procedural guides must be several pages long and highly
   detailed, including purpose, scope, roles, prerequisites, procedures, decision points,
   exceptions, controls, validation, troubleshooting, and expected outcomes.
2. **Excel workbooks:** Every Excel data workbook must contain at least 1,000 realistic data rows
   and more than one worksheet. Include researched business-appropriate columns, stable entity and
   source IDs, natural invented names, reference or lookup tabs, calculations, summaries, and charts
   where useful. Related workbooks must share the same style system and field conventions.
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

## Completion quality bar

Before reporting completion, verify every item in this checklist:

- The package root contains exactly one overview Page and one `demo/` folder.
- `demo/` contains only `DEMO-INSTRUCTIONS.docx` and `sample-data/`.
- No Markdown, manifest, README, repository metadata, or GitHub-posting guidance is generated.
- The Word presenter guide matches the reference guide's clean one-to-two-page design and contains
  only the scenario, exact demo tool or attached agent, exact files, and numbered prompt boxes, plus
  a concise build section when genuinely required.
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
- Public classification and the Microsoft Fake Company disclaimer remain present without making the
  presenter guide cluttered.
- Every final artifact is verified, every rendered guide page is visually inspected, and every
  uploaded file is present before completion is reported.
