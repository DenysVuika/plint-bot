# Project Lint Bot for GitHub

> Warning, the project is in the early development stage.
> To raise an issue or feature request, please use the following link: [plint-bot](https://github.com/DenysVuika/plint-bot)

This is a public repository for issue tracking and feature requests.

## Description

Provides linting support for your projects by utilizing various optional modules.

## History

For the list of changes, please refer to the [CHANGELOG](CHANGELOG.md)

## Modules

The application supports multiple opt-in modules.
Here's a list of modules that you can toggle for your projects:

* **Prettier**, performs code formatting checks with the "Fix" action support
* **Spellcheck**, performs spellcheck validation

## Configuration

You can provide the configuration in the `.github/plint.yml` file, for example:

```yaml
modules:
  - pr.prettier
  - pr.spellcheck

prettier:
  autoFix: true
  options:
    singleQuote: true
```

All configuration options are optional.

## Prettier Module

Powered by the [Prettier](https://prettier.io/) code formatter.

```yaml
modules:
  - pr.prettier

prettier:
  autoFix: true
  options:
    singleQuote: true
  exclude:
    - node_modules/**/*
```

### Options

For the list of options, please refer to the Prettier [documentation](https://prettier.io/docs/en/options.html).

### Exclude

You can provide a list of [minimatch](https://www.npmjs.com/package/minimatch) patterns to exclude content from the checks.

The following patterns are `always` excluded from the check:

```text
node_modules/**/*
package.json
package-lock.json
yarn.lock
tsconfig.json
plint.yml
```

## Spellcheck Module

Powered by the [cspell](https://github.com/Jason3S/cspell) library.

```yaml
modules:
  - pr.prettier
  - pr.spellcheck

spellcheck:
  words:
    - plint
  dictionaries:
    - html
    - en-gb
    - en_US
  exclude:
    - package.json
```

### Exclude

You can provide a list of [minimatch](https://www.npmjs.com/package/minimatch) patterns to exclude content from the checks.

The following patterns are `always` excluded from the check:

```text
node_modules/**/*
package.json
package-lock.json
yarn.lock
tsconfig.json
plint.yml
```