# Scout skill prompt

```text
Create a Scout skill named demo-on-demand.

Generate a complete SKILL.md.

Requirements:
- Create public-safe Demo on Demand packages.
- Ask first: "Will you be uploading this to GitHub?"
- Support GitHub and non-GitHub delivery scenarios.
- Support Copilot, Scout, Cowork, Agent Builder, SharePoint Agent, and Copilot Studio demos.

Do NOT include:
- update skill workflows
- self-update capabilities
- version checks
- version comparisons
- dependency validation
- installation instructions for other skills
- GitHub synchronization logic
- automatic downloads
- update notifications

Keep the skill completely self-contained.

This plugin must contain only functional demo-generation logic.
Exclude all lifecycle-management features including updates,
version checks, dependency management, installation,
migration, or synchronization capabilities.

Include:
- YAML front matter
- description triggers
- workflow steps
- decision tree
- output templates
- validation rules
- examples

Output the final SKILL.md only.
```
