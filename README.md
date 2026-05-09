# Kirisaki APM
Microsoft APM package meant for use by the Kirisaki team.

**Warning**: This repository is public for ease of use, any private and sensitive project information should not be put here.

## Installation
1. Install APM in your dev environment.
2. `apm init` the repo if it doesn't have an `apm.yml` file at the root.
3. Install the parts you want from APM.

### Install the whole package
This will install the content of all subpackages:
```bash
apm install visionshift/kirisaki_APM
```

### Install just a specific subpackage
Each subfolder in this repo containing an `apm.yml` file is its own subpackage.
For example to install just the `common` subpackage:
```bash
apm install visionshift/kirisaki_APM/common
```

### Pick and mix
If you just want specific AI primitives without installing the rest, just install the relevant folder (for skills) or `.md` file (for instructions, prompts, etc.):
```bash
# Skills require the folder:
apm install visionshift/kirisaki_APM/common/.apm/skills/devcontainer-aware-command-execution
# Self-contained primitives just need the .md file:
apm install visionshift/kirisaki_APM/common/.apm/instructions/filesystem-boundaries.instructions.md

```

## Updating
Every change to the AI primitives in this repo increments the packages' versions. APM pins installs to the versions it downloaded during install.

To update all of the APM dependencies to the latest versions, run:
```bash
apm install --update
```
