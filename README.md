# Repo Title
![GitHub last commit](https://img.shields.io/github/last-commit/wnndgws/boilerplate-repo)&nbsp;![GitHub top language](https://img.shields.io/github/languages/top/wnndgws/boilerplate-repo)&nbsp;![GitHub License](https://img.shields.io/github/license/wnndgws/boilerplate-repo)&nbsp;[![Versioning](https://img.shields.io/badge/version_scheme-EffVer-0097a7)](https://jacobtomlinson.dev/effver)&nbsp;![GitHub release](https://img.shields.io/github/v/release/wnndgws/boilerplate-repo)


## Description
Boilerplate templates for the project types I use most.
Each branch allows me to reference the tools for that project type.

1) [Repo Title](#repo-title)
   1) [Description](#description)
   2) [Quick Start](#quick-start)
      1) [Installation](#installation)
      2) [Usage](#usage)
      3) [Configuration](#configuration)
   3) [License](#license)


## Quick Start
There are 4 different boilerplate versions;
|#|Branch Name|Use Case|
|---|---|---|
|0| main (This One) | Boilerplate all repos have in common. Almost never the correct branch to use|
|1| python | If the main file is `python`|
|2| shell | If the main file is `zsh`, `bash`, or `sh`|
|3| text | If the main content is `markdown`, `txt`, or `LaTeX`|


### Installation
The easiest way to use this is to do the following steps:
* Clone the branch I want
* Delete the `.git` folder
* Init, add files, and commit to the new repo

> [!IMPORTANT]
> Change every `change-this` in the commands below

```zsh
git clone -b change-this --single-branch --depth 1 https://github.com/wnndgws/boilerplate-repo.git change-this
cd change-this
rm -rf .git
git init
xargs -n1 curl -s < gitignore_urls.txt >> .gitignore
xargs -n1 curl -s < repo_gitignore_urls.txt >> .gitignore
rm gitignore_urls.txt
rm repo_gitignore_urls.txt
git add -A
git commit -m "Initial commit"
gh repo create change-this --source=. --remote=origin --push --git-protocol ssh
```

### Usage
The `main` repo contains:
* `README.md`
* `LICENSE`
* A way to generate a `.gitignore`
* `git-crypt` setup to use my GPG keys

### Configuration
* To change which files get encrypted, make changes in `.gitattributes`

## License
This project is licensed under the GNU Affero General Public License v3.0.
See [LICENSE](./LICENSE) for details.
