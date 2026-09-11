# Personal installation

This archive contains demo-on-demand, generate-data, and demo-builder-style-guidelines. Install all
three from the same release. Keep companies.csv and names.csv beside generate-data/SKILL.md and
preserve all companion directories. Do not mix files from main into a released installation.

## Cowork

The Cowork ZIP has manifest.json and PNG icons at its root, with skill folders under skills/.
Ask Cowork to install it for your personal use through its supported installation capabilities.
If it can install only skill folders, it must clearly report that the M365 plugin was not registered.
Do not treat a ZIP download or temporary extraction as successful persistent installation.

If plugin registration is unavailable in chat, personal sideloading is documented at:
https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/cowork-plugin-development

With Node.js/npm and Microsoft 365 Agents Toolkit CLI installed:

```text
atk auth login
atk install --file-path ./cowork-plugin.zip --scope Personal
```

Complete authentication directly in the host or browser. Never paste credentials into a chat.
Tenant policy must allow personal sideloading. Retain the returned AppId and TitleId for later
updates or removal. Tenant-wide deployment and store publication are outside this release strategy.

## Scout

The Scout ZIP contains three skill folders at its root. Ask Scout to install those folders and all
support files into its configured personal skills location. Do not create a Cowork app registration
for this package. If multiple-skill ZIP installation is unsupported, extract and install each folder
through the supported skill installation mechanism.

## Verification and upgrades

- Report each installed skill's name, metadata version, and actual host-provided location.
- Read both approved CSVs through the installed generate-data skill and verify usable records.
- For Cowork, open all three presenter, quality, and technology references.
- Verify discovery in a new conversation; if the installer cannot do this, report it as unverified.
- Before replacing any existing skill, preview the changes and request confirmation. Do not delete
  unrelated skills or overwrite local edits silently. Avoid duplicate old and new registrations.
- Keep all shared dependencies from one release. Retain the Cowork app ID across plugin upgrades.

Automated package validation does not prove host installation support. The user must test actual
installation, persistence, activation, and demo behavior in Cowork and Scout.