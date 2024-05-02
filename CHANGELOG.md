# Changelog

<!-- next-header -->

## [Unreleased] - ReleaseDate

## [0.15.0] - 2024-05-01

> **Breaking Change Upgrade Note For Library Users**
>
> Due to the addition of additional naming strategies. You now need to pass `true` or `false` to the `Generator::new()` method.
> 
> ```rust
> <!-- No Numbering -->
> Generator::new(ADJECTIVES, NOUNS, naming, false)
> 
> <!-- Numbering -->
> Generator::new(ADJECTIVES, NOUNS, naming, true)
> ```
 
- New naming strategies types added to complment `Name:Plain` and `Name::Numbered`. The new namging stratgies are as followed:

  - Name::Plain **adjective-noun**
  - Name::Numbered  **adjective-noun-number**
  - Name::TitleCase **Adjective Noun**
  - Name::CamelCase **adjectiveNoun**
  - Name::ClassCase **AdjectiveNoun**
  - Name::KebabCase **adjective-noun**
  - Name::TrainCase **Adjective-Noun**
  - Name::TableCase **adjective-noun**
  - Name::SnakeCase **adjective_noun**
  - Name::PascalCase **AdjectiveNoun**
  - Name::SentenceCase **Adjective noun**
  - Name::ScreamingSnakeCase **Adjective_Noun**


### Changed

- upgrade to `regex` 1.10.4
- added `Inflector` 0.11.4, used with the naming strategy `to_*_case()` logic.

## [0.14.0] - 2022-06-28

### Changed

- upgrade to `regex` 1.5.6

## [0.13.0] - 2022-03-05

### Changed

- upgrade to `clap` version 3
- update other dependencies via `cargo update`

## [0.12.0] - 2021-09-12

> **Breaking Change Upgrade Note For Library Users**
>
> Due to the collapsing of a library crate and a binary/CLI crate into one
> crate, there is now a Cargo feature called `"application"` which is included
> in the default features. This allows for a clean `cargo install names`,
> resulting in a compilation and installation of the names CLI without any
> further options or flags. When using names as a library crate however, it is
> advised to now add `default-features = false` to the crate dependency in
> `Cargo.toml`. For example:
>
> ```toml
> [dependencies]
> names = { version = "0.12.0", default-features = false }
> ```
>
> This will exclude the `clap` crate when being used in library/crate mode.

### Changed

- **(breaking):** collapse library and binary into 1 dual-purpose crate which
  enables `cargo install names` to install the binary CLI
- **(breaking):** upgrade minimum supported Rust version to 1.46.0
- upgrade to `rand` 0.8.4
- upgrade to `clap` 3.0.0-beta.2
- update codebase to Rust 2018 edition and idioms

### Added

- cross platform matrix testing
- binary artifacts on each release for Linux, macOS, Windows, & FreeBSD systems
- nightly releases

## [0.11.0] - 2016-04-29

### Changed

- **(breaking):** move adjectives const to `names::ADJECTIVES`
- **(breaking):** move nouns const to `names::NOUNS`
- inline adjective and noun data from plaintext files

### Added

- (cli): add color and suggestions features

## [0.10.0] - 2015-11-01

### Changed

- **(breaking):** use `Default` trait for Generator & Name types
- (cli): update usage output

## [0.9.0] - 2015-09-15

The initial release.

<!-- next-url -->

[unreleased]: https://github.com/fnichol/names/compare/v0.14.0...HEAD
[0.14.0]: https://github.com/fnichol/names/compare/v0.13.0...v0.14.0
[0.13.0]: https://github.com/fnichol/names/compare/v0.12.0...v0.13.0
[0.12.0]: https://github.com/fnichol/names/compare/v0.11.0...v0.12.0
[0.11.0]: https://github.com/fnichol/names/compare/v0.10.0...v0.11.0
[0.10.0]: https://github.com/fnichol/names/compare/v0.9.0...v0.10.0
[0.9.0]: https://github.com/fnichol/names/compare/f852f53...v0.9.0
