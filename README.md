# cookiecutter-rye template (WIP)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Quick rye/pytest/yarn/actions setup for a pypi project

## Usage

* Install `rye` (possibly also `uv`) and `yarn` (or `npm`) the way you like it

* Run
```shell
pip install cookiecutter # or pipx install cookiecutter

# this creates the package directory structure according the `cookiecutter-rye` template
cookiecutter gh:ffreemt/cookiecutter-rye

# or cookiecutter https://github.com/ffreemt/cookiecutter-rye.git
```

* cd to the package directory
```bash
cd pack_name
```
* Run
```bash
# this installs some libs given in pyproject.toml
rye pin 3.12.0  # other python version
rye sync

# this installs npm-run-all given in package.json
yarn  # or npm install

```
Now you have a project set up and can start coding and change the world for the better;). For exmaple

```
rye add  httpx
rye sync  # or much faster:  uv install httpx 
```



* Shortcuts are set in package.json. Take a look and get a rough idea. For example
   * `yarn test`
   * `yarn style`: will run `black tests pack_name` and reload when any .py file is modified in `tests` and pack_name directories.

* build and publish
  * rye build
  * rye publish
