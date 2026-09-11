## Downloads

- **cowork-plugin.zip**: M365 schema 1.28 skills-only plugin for personal sideloading.
- **scout-skills.zip**: three installable skill folders, without Cowork app metadata.
- **SHA256SUMS.txt**: SHA-256 checksums of the ZIPs and release-info.json.
- **release-info.json**: package version, stable Cowork app ID, source commit, schema hash, and individual skill versions.

Both packages include demo-on-demand, generate-data with both approved CSVs, and shared style
guidance. Cowork also includes its presenter, quality, and technology references. Runtime skill
files do not self-update from main. Scout retains its GitHub/non-GitHub branch; Cowork remains
folder-native.

## Installation

Attach the matching ZIP to Cowork or Scout and ask it to install every bundled skill and companion
file for your personal use. Ask it to report the installed skill names, versions, locations, and
whether they remain available in a new conversation. Confirm replacement before overwriting any
existing skill, including shared dependencies.

Cowork should report whether it registered the M365 plugin or installed only its skill folders.
If chat cannot register the plugin, use personal sideloading with the Microsoft 365 Agents Toolkit:
`atk auth login`, then `atk install --file-path ./cowork-plugin.zip --scope Personal`.
Tenant policy must allow personal sideloading. Do not deploy to the tenant or submit to the store.

Chat-driven installation and runtime behavior require user acceptance testing. Automated checks
validate packaging, not host support or installation success. See the repository's deployment guide
for the complete test checklist and migration guidance.