# demo-on-demand 2.3.2-log

## Skill name

demo-on-demand

## Skill version

2.3.2

## Additions

- Moved Cowork runtime skill versioning from top-level `version` frontmatter to `metadata.version`
  for Agent Skills specification compatibility.
- Replaced undocumented top-level `cowork.category` and `cowork.icon` extension fields with string
  metadata values `cowork-category` and `cowork-icon`.
- Updated Cowork runtime version-check language to compare `metadata.version`.

## Deletions

- Removed non-standard top-level `version` frontmatter from the Cowork runtime skill.
- Removed undocumented top-level `cowork` frontmatter block from the Cowork runtime skill.
