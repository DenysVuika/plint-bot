# Project Lint Bot for GitHub

> Warning, the project is in the early development stage.
> To raise an issue or feature request, please use the following link: [plint-bot](https://github.com/DenysVuika/plint-bot)

This is a public repository for issue tracking and feature requests.

## Description

Provides linting support for your projects by utilizing various optional modules.

## Modules

Here's a list of modules that you can toggle for your projects:

* **Prettier**, performs code formatting checks with the "Fix" action support

## Configuration

You can provide the configuration in the `.github/plint.yml` file, for example:

```yaml
modules:
  - pr.prettier

prettier:
  autoFix: true
  options:
    singleQuote: true
```