# 🐍 MeynDev Python Guidelines

| Feature              | Tool                                                             | Purpose                                      |
|----------------------|------------------------------------------------------------------|----------------------------------------------|
| Project manager      | [uv](https://github.com/astral-sh/uv)                            | Dependency management & virtual environments |
| Linting & formatting | [ruff](https://github.com/astral-sh/ruff)                        | Code style, formatting & linting             |
| Import sorting       | [ruff (isort rules)](https://docs.astral.sh/ruff/rules/#isort-i) | Consistent and sorted imports                |
| Testing              | [pytest](https://docs.pytest.org/)                               | Writing and running tests                    |
| Building             | [Nuitka](https://nuitka.net/)                                    | Compile Python to native binaries            |
| Type checking        | [Pyright](https://github.com/microsoft/pyright)                  | Fast and lightweight type checking           |
| Pre-commit hooks     | [pre-commit](https://pre-commit.com/)                            | Automating code quality checks on commits    |

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
#### Don't forget to run `pre-commit autoupdate` for replace "latest" ro actual latest versions.
