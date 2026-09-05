# Repo Title
![GitHub last
commit](https://img.shields.io/github/last-commit/wnndgws/boilerplate-repo)
![GitHub top
language](https://img.shields.io/github/languages/top/wnndgws/boilerplate-repo)
![GitHub License](https://img.shields.io/github/license/wnndgws/boilerplate-repo)␠
                                                                                 [![Versioning](https://img.shields.io/badge/version_scheme-EffVer-0097a7)](https://jacobtomlinson.dev/effver)


## Description
Boilerplate templates for the project types I use most.
Each branch allows me to reference the tools for that project type.
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
git add -A
git commit -m "Initial commit"
gh repo create change-this --source=. --remote=origin --push --git-protocol ssh

```

### Usage
The `main` repo contains:
* `README.md`
* `LICENSE`
* `.gitignore`

### Configuration

## License
This project is licensed under the GNU Affero General Public License v3.0.
See [LICENSE](./LICENSE) for details.
