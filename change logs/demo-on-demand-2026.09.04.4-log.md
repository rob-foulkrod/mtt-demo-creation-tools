# demo-on-demand 2026.09.04.4-log

## Skill name

demo-on-demand

## Skill version

2026.09.04.4

## Additions

- Added explicit guidance that newly created demos must not be logged to a shared catalog, SharePoint folder, workbook, list, or other tracking destination until a future logging process is selected.
- Added guidance to use `https://github.com/rob-foulkrod/mtt-demo-creation-tools` as the source for demo-builder skill updates and documentation.
- Updated final reporting guidance so published GitHub demos report only the created repository URL and generated package contents, without creating a separate catalog row.
- Updated generate-data dependency guidance to require version `2026.09.04.4` or newer.

## Deletions

- Removed the mandatory shared Demo-on-Demand catalog workbook workflow.
- Removed references to the former SharePoint demo catalog location under `CA West Team IdeaHub`.
- Removed catalog archive/delete/update validation requirements from the cleanup and quality-bar sections.
