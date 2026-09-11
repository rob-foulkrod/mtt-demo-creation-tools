# demo-on-demand 2.4.0-log

## Skill name
demo-on-demand (Cowork)

## Skill version
2.4.0

## Additions
- Load bundled data and style skills from the same release using host-resolved locations.
- Stop affected generation when the installation is incomplete; retain local data validation.
- Use the bundled Markdown presenter specification without an external Word template.
- Keep overwrite protection and named confirmation for deletion explicit in the packaged runtime.

## Deletions
- Runtime version checks, mutable-main instruction replacement, and dependency downloads.
- Creator-maintenance directives in the runtime skill.
- References to the absent DEMO-INSTRUCTIONS-REFERENCE.docx file.