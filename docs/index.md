

<p align="center">
  <img width="600" src="static/cookiecutter.svg">
</p style = "margin-bottom: 2rem;">
<style>
  .md-typeset h1,
  .md-content__button {
    display: none;
  }
</style>

---

[![Release](https://img.shields.io/github/v/release/fpgmaas/cookiecutter-poetry)](https://pypi.org/project/cookiecutter-poetry/)
[![Build status](https://img.shields.io/github/actions/workflow/status/fpgmaas/cookiecutter-poetry/main.yml?branch=main)](https://github.com/fpgmaas/cookiecutter-poetry/actions/workflows/main.yml?query=branch%3Amain)
[![Supported Python versions](https://img.shields.io/pypi/pyversions/cookiecutter-poetry)](https://pypi.org/project/cookiecutter-poetry/)
[![License](https://img.shields.io/github/license/fpgmaas/cookiecutter-poetry)](https://img.shields.io/github/license/fpgmaas/cookiecutter-poetry)

This is a [cookiecutter](https://github.com/cookiecutter/cookiecutter)
repository to generate the file structure for a Python project that uses
[Poetry](https://python-poetry.org/) for its dependency management. 

A project generated with ``cookiecutter-poetry`` supports the following features:

- [Poetry](https://python-poetry.org/) for dependency management
- CI/CD with [GitHub Actions](https://github.com/features/actions)
- Pre-commit hooks with [pre-commit](https://pre-commit.com/)
- Formatting with [black](https://pypi.org/project/black/) and [isort](https://pycqa.github.io/isort/index.html)
- Linting with [flake8](https://flake8.pycqa.org/en/latest/)
- Static type checking with [mypy](https://mypy.readthedocs.io/en/stable/)
- Dependency checking with [cookiecutter-poetry](https://fpgmaas.github.io/cookiecutter-poetry/)
- Publishing to [Pypi](https://pypi.org) or [Artifactory](https://jfrog.com/artifactory) by creating a new release on GitHub
- Testing with [pytest](https://docs.pytest.org/en/7.1.x/)
- Test coverage with [codecov](https://about.codecov.io/)
- Documentation with [MkDocs](https://www.mkdocs.org/)
- Compatibility testing for multiple versions of Python with [Tox](https://tox.wiki/en/latest/)
- Containerization with [Docker](https://www.docker.com/)

An example of a repository generated with this package can be found [here](https://github.com/fpgmaas/cookiecutter-poetry-example).

## Quickstart

On your local machine, navigate to the directory in which you want to
create a project directory, and run the following two commands:

``` bash
pip install cookiecutter-poetry 
ccp
```

Alternatively, install `cookiecutter` and directly pass the URL to this
Github repository to the `cookiecutter` command:

``` bash
pip install cookiecutter
cookiecutter https://github.com/fpgmaas/cookiecutter-poetry.git
```

Create a repository on GitHub, and then run the following commands, replacing `<project-name>`, with the name that you gave the Github repository and
`<github_author_handle>` with your Github username.

``` bash
cd <project_name>
git init -b main
git add .
git commit -m "Init commit"
git remote add origin git@github.com:<github_author_handle>/<project_name>.git
git push -u origin main
```

Finally, install the environment and the pre-commit hooks with

```bash
make install
```

You are now ready to start development on your project! The CI/CD
pipeline will be triggered when you open a pull request, merge to main,
or when you create a new release.

To finalize the set-up for publishing to PyPi or Artifactory, see [here](./features/publishing.md#set-up-for-pypi). For activating the automatic documentation with MkDocs, see [here](./features/mkdocs.md#enabling-the-documentation-on-github). To enable the code coverage reports, see [here](./features/codecov).

## Acknowledgements

This project is partially based on [Audrey
Feldroy's](https://github.com/audreyfeldroy) great
[cookiecutter-pypackage](https://github.com/audreyfeldroy/cookiecutter-pypackage).

