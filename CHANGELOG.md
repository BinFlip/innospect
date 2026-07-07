# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.2] - 2026-07-06

### Added

- Codepage-aware string decoding via `LanguageCodepage::decode`: UTF-16LE for
  modern Unicode builds and Windows ANSI code pages (cp1251 / cp1252 / cp932 / …)
  for legacy installers, with a lossy replacement fallback for unmappable pages.
  `LanguageEntry` name / language-name accessors now decode through it.
- Public `from_raw` inverse constructors on record enums, for reconstructing
  typed values from stored raw discriminants: `FileEntryType`, `SignMode`,
  `Bitness`, `DeleteTargetType`, `CloseOnExit`, `RunWait`, `SetupTypeKind`,
  `RegistryHive`, `RegistryValueType`, and `LanguageCodepage`.

### Changed

- Bumped dependencies: `bitflags` 2.11.1 → 2.13.0, `goblin` 0.10.5 → 0.10.7,
  `chacha20` 0.10.0 → 0.10.1.

### Added (dependencies)

- `encoding_rs` 0.8.35 and `codepage` 0.1.2, for the codepage-aware decoding above.

## [0.1.1] - 2026-06-09

- Initial published release.

[0.1.2]: https://github.com/BinFlip/inno-rs/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/BinFlip/inno-rs/releases/tag/v0.1.1
