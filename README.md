# GitHub Action - installing necessary PIP modules and linting tools

Installing necessary PIP modules and Linting tools

It performs the following things:
* Installing of necessary PIP modules according to requirements.txt and requirements-lint.txt
* Installing Linting tools:
** shellcheck
** yamllint
** flake8
** pylint

## Example

```yaml
  steps:
    - uses: actions/checkout@v4
    - uses: fbrehm/prepare-debian-container@v1
    - uses: fbrehm/github-install-pip-modules
      with:
        install_pytest: true
```

## Inputs

```yaml
inputs:
  install_pytest:
    description: Should pytest be installed.
    required: false
    default: false
  install_linter_tools:
    description: Should linter tools like pylint, flake8, shellcheck a.s.o be installed.
    required: false
    default: false
```

