# LaTeX Report

:warning: Packages requiring Shell Escape [are not supported](https://github.com/tectonic-typesetting/tectonic/issues/38)

:information_source: Source code is cached and re-generated when they have changed.

## Requirements

- Linux, macOS or Windows Subsystem for Linux*
- [miniconda]
- pygments
- tectonic

\* Tectonic does not natively support Windows currently

## Setup

1. Install [miniconda]
2. `conda config --add channels conda-forge`
3. `conda update --all`
4. `conda install pygments tectonic`

## Continuous Deployment

Travis can automate the PDF generation which can be accessed within the `report` branch.

- Go to your profile on https://travis-ci.org
  - Private repositories are only on https://travis-ci.com (free with GitHub Education)
- Enable the repository (e.g `wopian/latex-bnu`)
- Click the :gear: icon beside the toggle
- Enable `Build only if .travis.yml is present`
- Add a `GH_TOKEN` environment variable
  - [Generate a new token](https://github.com/settings/tokens) on GitHub
    - Tick only `public_repo` for public repositories
    - Tick only `repo` for private repositories

## Commands

- `bin/report` - full build of the LaTeX project
- `bin/pyg` - generate syntax highlighted TeX files of source code only
- `bin/tex` - generate PDF from LaTeX files only

### Windows

To run these commands on Windows, either:
- Enter into a bash shell and run the commands or (`bash` -> `bin/report` -> `exit`)
- Run bash in interactive mode in CMD or PowerShell (`bash -i bin/report`)

[miniconda]: https://conda.io/miniconda.html
