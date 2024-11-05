# madge pre-commit hooks

This repository provides [Mage](https://www.npmjs.com/package/madge) hooks for [pre-commit](https://pre-commit.com/).

The following section assumes that you [installed pre-commit](https://pre-commit.com/index.html#install) and run `pre-commit install` in your repository.

## Using madge pre-commit hooks

| hook `id` | description                                           |
|-----------|-------------------------------------------------------|
| `madge`   | Check for circular dependencies in the provided paths |

For example, if you want to use the `madge` hook,
add the following pre-commit configuration to the root of your project in a file named `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/B-S-F/madge-pre-commit
    rev: ""  # Use the sha / tag you want to point at
    hooks:
      - id: madge
        args: [src]
```