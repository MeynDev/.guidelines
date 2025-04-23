# 🐍 MeynDev Python Guidelines

| Feature              | Tool                                                                                                                                             | Purpose                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Project manager      | [![uv](https://img.shields.io/badge/uv-DE5FE9?style=for-the-badge&logo=uv&logoColor=white)](https://github.com/astral-sh/uv)                     | Dependency management & virtual environments |
| Linting & formatting | [![ruff](https://img.shields.io/badge/ruff-D7FF64?style=for-the-badge&logo=ruff&logoColor=black)](https://github.com/astral-sh/ruff)             | Code style, formatting & linting             |
| Testing              | [![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)](https://pytest.org)                      | Writing and running tests                    |
| Building             | [![Nuitka](https://img.shields.io/badge/nuitka-3776AB?style=for-the-badge&logo=nuitka&logoColor=white)](https://nuitka.net)                      | Compile Python to native binaries            |
| Type checking        | [![Pyright](https://img.shields.io/badge/Pyright-C3C38F?style=for-the-badge&logo=pyright&logoColor=white)](https://github.com/microsoft/pyright) | Fast and lightweight type checking           |
| Pre-commit hooks     | [![pre-commit](https://img.shields.io/badge/pre--commit-FAB040?style=for-the-badge&logo=pre-commit&logoColor=black)](https://pre-commit.com)     | Automating code quality checks on commits    |

## Basic pre-commit hooks configuration for linting, formatting and type checking
```yaml
repos:
- repo: https://github.com/pre-commit/pre-commit-hooks
  rev: latest
  hooks:
    - id: trailing-whitespace
    - id: end-of-file-fixer
    - id: check-yaml
    - id: check-added-large-files

- repo: https://github.com/astral-sh/ruff-pre-commit
  rev: latest
  hooks:
    - id: ruff
      args: [ --fix ]
    - id: ruff-format

- repo: https://github.com/RobertCraigie/pyright-python
  rev: latest
  hooks:
  - id: pyright
    language: system

```
#### Don't forget to run `pre-commit autoupdate` for replace "latest" to actual latest versions.

## How to create project
1. Init project using uv:
   ```shell
   uv init ZapFiles-rewritten && cd ZapFiles-rewritten
   ```
2. Create and activate venv (Linux)
   ```shell
   uv venv && source .venv/bin/activate
   ```
