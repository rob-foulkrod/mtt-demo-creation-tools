# demo-on-demand 2.2.2-log

## Skill name

demo-on-demand

## Skill version

2.2.2

## Additions

- Added the public change logs folder reference: `https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/change%20logs`.
- Added a requirement that every future Cowork demo builder skill update writes a versioned change log file.
- Defined the required change log file name format: `<skill-name>-<skill-version>-log.md`.
- Defined the required change log title format: `<skill-name> <skill-version>-log`.
- Required `Skill name`, `Skill version`, `Additions`, and `Deletions` sections in each log.
- Updated the generate-data dependency requirement to version `2026.09.04.3` or newer.
- Updated the Cowork skill update workflow so the change log is written before committing the skill update.

## Deletions

None
