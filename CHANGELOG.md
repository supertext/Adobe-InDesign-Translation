# Changelog

All notable changes to this project are documented here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project uses [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Security

- Import with translated copies: the language taken from the imported file goes into the copy's file name only as letters, digits, `-` and `_`, so a crafted file can't make the script write the copy into another folder.

### Added

- Support: the Supertext support form is linked in the README, the user guide and GitHub's "New issue" page.

### Changed

- Installation and developer guides: example paths use InDesign 2027 (`Version 22.0`), the current release.

## [1.0.0] - 2026-10-05

### Added

- `Translation Export.jsx`: exports all stories, table cells and footnotes to XLIFF 1.2, one file per target language, with persistent `SupertextID` story labels, paragraph-level trans-units, `<g>` inline formatting tags, `<x>` tags for forced line breaks, tabs and protected objects, and context notes.
- `Translation Import.jsx`: imports translated XLIFF into per-language copies as one undo step, keeps paragraph styles and objects in place, restores character formatting, skips content changed since export, rejects missing or reordered object tags, pauses Track Changes, unlocks locked layers, and reports overset text.
- `tests/logic-test.js`: tests the core logic against a mock of InDesign's text model.
- Installation guide, user guide and developer guide.

### Known issues

- Not yet tested in InDesign. Run the test checklist in the developer guide before production use.
