# MTT Demo Creation Tools

Public skill repository for MTT demo-on-demand tooling used by Scout and Cowork.

## Installing locally

Download the raw skill file and any required support files from the canonical URLs above, then place
them in the local skill folder used by Scout or Cowork. For generate-data, install `SKILL.md`,
`companies.csv`, and `names.csv` together so name and company validation can run locally.

Before running either demo builder skill, validate that its local `SKILL.md` exists and that the
generate-data folder contains all three required files. If a file is missing, download it from the
full public GitHub URL rather than relying on a relative path.

## Prompt: install everything for Scout

Use this prompt in Scout to install or refresh the Scout demo builder and the shared generate-data
dependency:

```text
Install these two skills from https://github.com/rob-foulkrod/mtt-demo-creation-tools

- scout/demo-on-demand-SKILL.md → install as skill "demo-on-demand"
- Common/generate-data/ → install as "generate-data", including companies.csv and names.csv
```

## Prompt: install everything for Cowork

Use this prompt in Cowork to install or refresh the Cowork demo builder and the shared generate-data
dependency:

```text
Install these two skills from https://github.com/rob-foulkrod/mtt-demo-creation-tools

- cowork/demo-builder-SKILL.md → install as skill "demo-on-demand"
- Common/generate-data/ → install as "generate-data", including companies.csv and names.csv
```



## Repository layout

| Path | Purpose |
| --- | --- |
| [`scout/demo-on-demand-SKILL.md`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/scout/demo-on-demand-SKILL.md) | Scout demo builder skill. It asks whether the package will be uploaded to GitHub, then creates either a GitHub-ready public demo repository package or a Cowork-compatible folder package. |
| [`cowork/demo-builder-SKILL.md`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/cowork/demo-builder-SKILL.md) | Cowork demo builder skill. It creates private-delivery, folder-native demo packages for OneDrive or SharePoint destinations. |
| [`Common/generate-data/SKILL.md`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/Common/generate-data/SKILL.md) | Shared generate-data compliance skill used before creating fictional companies, people, email addresses, or sample data. |
| [`Common/generate-data/companies.csv`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/Common/generate-data/companies.csv) | Approved fictitious company and domain list used by the generate-data skill. |
| [`Common/generate-data/names.csv`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/blob/main/Common/generate-data/names.csv) | Approved person-name list used by the generate-data skill. |
| [`change logs/`](https://github.com/rob-foulkrod/mtt-demo-creation-tools/tree/main/change%20logs) | Versioned skill change logs documenting additions and deletions for every skill update. |

## How versioning works

Each skill carries its own version in frontmatter and in its version section:

| Skill | Current version | Canonical source |
| --- | --- | --- |
| Scout demo builder | `2026.09.04.3` | `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/scout/demo-on-demand-SKILL.md` |
| Cowork demo builder | `2.2.2` | `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/cowork/demo-builder-SKILL.md` |
| Generate data | `2026.09.04.3` | `https://raw.githubusercontent.com/rob-foulkrod/mtt-demo-creation-tools/main/Common/generate-data/SKILL.md` |

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
3. Create a change log file in `change logs/` for every updated skill.
4. Name each log file `<skill-name>-<skill-version>-log.md`, for example `generate-data-2026.09.04.3-log.md`.
5. Give each log file the title `<skill-name> <skill-version>-log`.
6. Include `Skill name`, `Skill version`, `Additions`, and `Deletions` sections. If there are no deletions, write `None`.
7. Keep every source reference as a full public GitHub URL.
8. Commit and push the skill and change log changes together to `https://github.com/rob-foulkrod/mtt-demo-creation-tools`.
9. Update local installed copies from the canonical raw GitHub URLs.

