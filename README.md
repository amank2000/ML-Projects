# ML-Projects

Repo to work on ML projects

## Development setup

This repository uses [pre-commit](https://pre-commit.com/) to run formatters and linters
such as [Black](https://black.readthedocs.io/), [Ruff](https://github.com/astral-sh/ruff),
[Flake8](https://flake8.pycqa.org/), and [Mypy](https://mypy.readthedocs.io/). Basic
housekeeping hooks keep the tree spotless by trimming trailing whitespace and fixing
missing end-of-file newlines.
 
Install pre-commit and activate the hooks:

```bash
pip install pre-commit
pre-commit install
```

### Branch protection

Commits directly to the `main` branch are blocked by the `no-commit-to-branch` hook.
It is recommended to enable GitHub branch protection so that changes to `main` can
only be merged via pull requests after the CI pipeline succeeds.

### Merge strategy and cleanup

Configure the repository to allow only **Squash and merge** so that pull requests
are reduced to a single commit on `main`. Enable **Automatically delete head
branches** in repository settings to remove topic branches after a pull request
is merged. A companion workflow, `Delete merged branches`, also cleans up merged
branches for repositories where automatic branch deletion is not enabled.
