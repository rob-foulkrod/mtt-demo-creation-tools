# MTT Demo Creation Tools

Public skill repository for MTT demo-on-demand tooling used by Scout and Cowork.

## Repository layout

| Path | Purpose |
| --- | --- |
| [`scout/demo-on-demand-SKILL.md`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/scout/demo-on-demand-SKILL.md) | Scout demo builder skill. It asks whether the package will be uploaded to GitHub, then creates either a GitHub-ready public demo repository package or a Cowork-compatible folder package. |
| [`cowork/demo-builder-SKILL.md`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/cowork/demo-builder-SKILL.md) | Cowork demo builder skill. It creates private-delivery, folder-native demo packages for OneDrive or SharePoint destinations. |
| [`Common/generate-data/SKILL.md`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/Common/generate-data/SKILL.md) | Shared generate-data compliance skill used before creating fictional companies, people, email addresses, or sample data. |
| [`Common/generate-data/companies.csv`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/Common/generate-data/companies.csv) | Approved fictitious company and domain list used by the generate-data skill. |
| [`Common/generate-data/names.csv`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/Common/generate-data/names.csv) | Approved person-name list used by the generate-data skill. |

## How versioning works

Each skill carries its own version in frontmatter and in its version section:

| Skill | Current version | Canonical source |
| --- | --- | --- |
| Scout demo builder | `2026.09.04.2` | `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/scout/demo-on-demand-SKILL.md` |
| Cowork demo builder | `2.2.1` | `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/cowork/demo-builder-SKILL.md` |
| Generate data | `2026.09.04.2` | `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md` |

At the start of a run, the installed skill should check its canonical raw GitHub URL. If the public
copy has a higher version, it should tell the user and offer to download and install the updated
local copy before continuing. If the check cannot be completed, the skill can continue with the
installed version while disclosing that the update check was skipped.

## Generate-data dependency

Both demo builder skills depend on the shared generate-data skill whenever a package needs
fictional companies, people, email addresses, or sample data. The complete dependency is the full
folder at:

`https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data`

Install all three files together:

1. `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md`
2. `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/companies.csv`
3. `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/names.csv`

If the generate-data skill or either CSV is missing locally, the invoking demo builder skill should
offer to download and install the folder before it generates any data.

## Updating skills

1. Edit the skill file in this repository.
2. Increment the skill version. Use date-style versions for Scout and generate-data files, and semantic versions for the Cowork skill.
3. Keep every source reference as a full public GitHub URL.
4. Commit and push the changes to `https://github.com/rob-foulkrod/mtt-demo-creation-tools`.
5. Update local installed copies from the canonical raw GitHub URLs.

## Installing locally

Download the raw skill file and any required support files from the canonical URLs above, then place
them in the local skill folder used by Scout or Cowork. For generate-data, install `SKILL.md`,
`companies.csv`, and `names.csv` together so name and company validation can run locally.

Default local paths on this machine:

| Component | Default local path |
| --- | --- |
| Scout demo builder skill | `C:\Users\anconnif\.scout\m-skills\demo-on-demand\SKILL.md` |
| Cowork demo builder skill | `C:\Users\anconnif\.scout\m-skills\demo-on-demand\SKILL.md` |
| Generate-data folder | `C:\Users\anconnif\.scout\m-skills\generate-data` |
| Generate-data skill | `C:\Users\anconnif\.scout\m-skills\generate-data\SKILL.md` |
| Approved companies CSV | `C:\Users\anconnif\.scout\m-skills\generate-data\companies.csv` |
| Approved names CSV | `C:\Users\anconnif\.scout\m-skills\generate-data\names.csv` |

Before running either demo builder skill, validate that its local `SKILL.md` exists and that the
generate-data folder contains all three required files. If a file is missing, download it from the
full public GitHub URL rather than relying on a relative path.

## Prompt: install everything for Scout

Use this prompt in Scout to install or refresh the Scout demo builder and the shared generate-data
dependency:

```text
Install the Scout demo builder skill from https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/scout and install the shared generate-data dependency from https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data. Download the raw files from the public GitHub URLs, place the Scout skill at C:\Users\anconnif\.scout\m-skills\demo-on-demand\SKILL.md, place generate-data at C:\Users\anconnif\.scout\m-skills\generate-data, and verify that generate-data includes SKILL.md, companies.csv, and names.csv before reporting completion.
```

## Prompt: install everything for Cowork

Use this prompt in Cowork to install or refresh the Cowork demo builder and the shared generate-data
dependency:

```text
Install the Cowork demo builder skill from https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/cowork and install the shared generate-data dependency from https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/Common/generate-data. Download the raw files from the public GitHub URLs, place the Cowork skill in the active Cowork personal skill folder, place generate-data at C:\Users\anconnif\.scout\m-skills\generate-data unless a different local skill root is configured, and verify that generate-data includes SKILL.md, companies.csv, and names.csv before reporting completion.
```
