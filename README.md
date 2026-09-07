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
   3) [Preferred Python tools](#preferred-python-tools)
   4) [License](#license)


## Quick Start
There are 4 different boilerplate versions;
|#|Branch Name|Use Case|
|---|---|---|
|0| main| Boilerplate all repos have in common. Almost never the correct branch to use|
|1| python (This One) | If the main file is `python`|
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

## Preferred Python tools

|Package|Equivalent|Use-case|
|---|---|---|
|alive-progress |tqdm |Progress bars with live ETA/throughput that stay readable under heavy output|
|apscheduler |schedule / cron |Async-first in-process job scheduling with persistent job stores|
|cachebox |cachetools / functools.lru_cache |Fast in-process caches and memoisation with LRU/FIFO/LFU policies (Rust-backed)|
|duckdb |tinydb / SQLite (analytical) |Embedded columnar SQL database; query Parquet/CSV/JSON locally, first-class Polars interchange|
|granian |uvicorn / gunicorn |Rust ASGI/RSGI server for FastAPI apps, RSGI-native performance|
|hypothesis |parameterised pytest cases |Property-based testing; generate inputs and shrink failures automatically|
|httpx |requests |Sync and async HTTP client, ASGI transport for testing FastAPI apps|
|humanize |inflect |Readable quantities ("3 days ago", "1.2 MB")|
|joblib |pickle |Fast, disk-cached persistence of NumPy-heavy objects and parallelism|
|loguru |logging |Zero-config logging with rotation, colour, sane defaults|
|markupever |BeautifulSoup4 / lxml |Fast HTML/XML parsing with CSS selectors and DOM manipulation (Rust-backed)|
|maturin |setuptools + Cython |Build/publish PyO3 Rust extensions to PyPI with one command|
|msgspec |pydantic (wire formats) / msgpack |Ultra-fast typed msgpack/JSON schemas and serialisation|
|orjson |json |Fast JSON serialisation of large payloads (Rust-backed)|
|pathlib |os.path |Object-oriented filesystem paths (this is the modern replacement)|
|plumbum |subprocess / shell |Composable shell pipelines and remote commands in pure Python|
|polars |pandas |DataFrame queries with lazy execution, multi-threading, low memory|
|py-spy |cProfile / pyinstrument |Sampling profiler for running processes, flame graphs, zero instrumentation|
|pydantic |dataclasses + marshmallow |Typed, validated data models with serialisation|
|pyright |mypy |Static type checking (VS Code-native, fast, strict by default)|
|pytest |unittest |Ergonomic test runner with fixtures and parametrisation|
|python-statemachine |transitions |Declarative state machines with validation, events, and diagram output|
|questionary |input() / prompt_toolkit |Polished interactive CLI prompts (choices, confirm, autocomplete)|
|regex |re |Patterns beyond stdlib: recursion, fuzzy matching, POSIX classes|
|rich |colorama / manual ANSI |Terminal formatting, tables, trees, RichHandler for logs|
|robyn |FastAPI/Flask |Fast web services on a Rust runtime with built-in workers|
|tenacity |retrying |Retry with backoff for flaky calls (HTTP, networks)|
|thefuzz |fuzzywuzzy |String similarity ratios and partial matching (maintained fork)|
|tomllib |configparser |Stdlib TOML parsing (the modern config format)|
|typer |argparse (+ click) |CLI apps from type hints; built on click|
|uv |pip / poetry / pyenv / pipx |All-in-one Rust package manager, lockfiles, Python installs|
|uvloop |asyncio |Drop-in asyncio event loop replacement built on libuv|
|whenever |datetime (+ dateutil/arrow) |Timezone-aware datetimes and durations without datetime footguns|


## License
This project is licensed under the GNU Affero General Public License v3.0.
See [LICENSE](./LICENSE) for details.
