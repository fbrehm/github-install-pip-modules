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
    - uses: actions/checkout@v
    - uses: fbrehm/prepare-debian-container@v1
    - uses: fbrehm/github-install-pip-modules
```

## Inputs

This action has no inputs.

