# generate-data 2026.09.11.2-log

## Skill name

generate-data

## Skill version

2026.09.11.2

## Additions

- Made generate-data solely responsible for validating and reading its own `companies.csv` and `names.csv` companion files using paths relative to its skill root.
- Defined missing, empty, unreadable, malformed, and unusable companion-file behavior.
- Added a handoff contract for approved company names, approved domains, approved person names, role placeholders, replacement tables, and validation summaries.
- Added PowerShell tests covering complete, missing, empty, and malformed companion-file cases.

## Deletions

None
