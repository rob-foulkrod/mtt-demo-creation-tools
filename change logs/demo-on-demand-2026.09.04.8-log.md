# demo-on-demand 2026.09.04.8-log

## Skill name

demo-on-demand

## Skill version

2026.09.04.8

## Additions

- Moved Scout runtime skill versioning from top-level `version` frontmatter to `metadata.version`
  for Agent Skills specification compatibility.
- Updated Scout runtime version-check language to compare `metadata.version`.

## Deletions

- Removed non-standard top-level `version` frontmatter from the Scout runtime skill.
