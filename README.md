# action-pytest

A composite action that tests a project with [pytest](https://docs.pytest.org/en/stable/).

This repository is not meant to be referenced in third-party workflows; please fork the repository if you would like to use it in your project.

## Inputs

| Name              | Description                                       | Default |
| ----------------- | ------------------------------------------------- | ------- |
| cache             | Whether to cache project dependencies.            | "true"  |
| coverage          | Whether to generate a coverage report.            | "true"  |
| package_manager   | The package manager to use ("poetry" or "uv").    | "uv"    |
| python_version    | The python version to use in SemVer range syntax. | "3.13"  |
| working_directory | The working directory for the action.             | "."     |

## Examples

### Without coverage

```
jobs:
  python:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-pytest@main
        with:
          cache: "true"
          coverage: "false"
          package_manager: uv
          python_version: "3.13"
```

### With coverage

```
jobs:
  python:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-pytest@main
        with:
          cache: "true"
          coverage: "true"
          package_manager: uv
          python_version: "3.13"
```

## License

action-pytest is released under the [MIT License](./LICENSE)
