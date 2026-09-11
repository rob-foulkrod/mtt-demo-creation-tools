# Plugin package prompt

```text
Create a Microsoft 365 Copilot Cowork plugin package.

Naming Requirements:
- If the source skill is named <skill-name>, the plugin version MUST be named <skill-name>-plugin.
- All generated folders, manifests, and references should use the -plugin suffix.

Generate:

- manifest.json
- color.png placeholder
- outline.png placeholder
- skills/<skill-name>-plugin/SKILL.md

Purpose:
Create Demo on Demand packages for Microsoft Technical Trainers (MTTs).

Workflow:
1. Ask whether the package will be published to GitHub.
2. If Yes:
   - Generate a GitHub-ready repository structure.
   - Create README.md.
   - Create setup instructions.
   - Create demo instructions.
   - Create sample public-safe content.
3. If No:
   - Generate a Cowork-compatible package.
   - Create a demo folder structure.
   - Create facilitator instructions.
   - Create learner instructions.

Support:
- Copilot
- Scout
- Cowork
- Agent Builder
- SharePoint Agent
- Copilot Studio

Restrictions:
- Public-safe content only.
- No confidential Microsoft information.
- No customer information.
- No copyrighted source material.

IMPORTANT:
- Do NOT generate update-checking workflows.
- Do NOT generate version-comparison logic.
- Do NOT generate self-update capabilities.
- Do NOT generate install-update skills.
- Do NOT include skill synchronization workflows.
- Do NOT reference newer versions of the skill.
- Do NOT include skill dependency validation.
- Do NOT include automatic download or installation instructions for other skills.
- Do NOT include GitHub version verification logic.

The plugin should be completely self-contained.

This plugin must contain only functional demo-generation logic.
Exclude all lifecycle-management features including updates,
version checks, dependency management, installation,
migration, or synchronization capabilities.

Generate:
- complete folder structure
- complete manifest.json
- complete SKILL.md
- example prompts
- example outputs
- validation rules

Follow Microsoft 365 Cowork plugin packaging conventions.
```
