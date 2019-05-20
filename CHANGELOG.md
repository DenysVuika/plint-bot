# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.3.1] - 2019-05-20

## Fixed

- `prettier` module shows valid files in error report
- `spellcheck` not using default dictionaries

## [1.3.0] - 2019-05-19

### Added

- report generation for `pr.prettier` module
- report generation for `pr.spellcheck` module

### Changed

- update `prettier` to 1.17.1
- update `probot` to 9.2.11

## [1.2.0]

### Added

- backend database support (mongodb)

## [1.1.2]

### Added

- Support for `exclude` patterns (minimatch)
- Exclude `node_modules` folder by default

## [1.1.1] - 2019-04-19

### Added

- Raise a pending status for each check at startup

### Fixed

- Handle crash when status check report is too long
- Handle crash when checking 1MB+ files

## [1.1.0] - 2019-04-18

### Added

- Code style check with Prettier
- Spellcheck support with cspell
