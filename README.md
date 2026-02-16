# Migrate to Dart null safety

> [!NOTE]
> **This repository contains archived documentation.**
> The guides in this repository were written between 2020 and 2023,
> during the rollout of null safety in Dart.
> They are preserved here for developers migrating legacy
> pre-null-safety codebases and for historical reference.
>
> Some details, tools, and links might be outdated.
> If you are **not** migrating a pre-null-safety codebase,
> you are better served by the current Dart documentation:
>
> - **[Dart language tour](https://dart.dev/language)** -
>   Learn Dart as it exists today, with sound null safety built in.
> - **[Dart type system](https://dart.dev/language/type-system)** -
>   Understand Dart's sound type system, including nullability.
> - **[Effective Dart](https://dart.dev/effective-dart)** -
>   Best practices for writing modern, idiomatic Dart.

Null safety was the largest change to the [Dart](https://dart.dev) language
since the introduction of its sound static type system in Dart 2.0.
With null safety, types are non-nullable by default:
a variable of type `String` always contains a string,
and a variable of type `String?` can contain either a string or `null`.
This guarantee is enforced at compile time, catching null-reference errors
before they reach production.

Null safety was introduced in Dart 2.12 (March 2021)
and became mandatory in Dart 3 (May 2023).
The documentation here was originally hosted on [dart.dev][] and
has been moved to this repository for archival purposes.

## Documentation and guides

- **[Sound null safety overview](docs/index.md)** -
  A starting point for understanding null safety in Dart.
  Covers the core principles, explains how to enable null safety
  across Dart 2.x and 3.x versions, and links to more detailed resources.

- **[Understanding null safety](docs/concepts.md)**

  A deep-dive article by Bob Nystrom that explains *how*
  Dart's type system handles `null`, *why* the design decisions were made, and
  how to write idiomatic null-safe Dart code.
  Covers nullable and non-nullable types, flow analysis,
  type promotion, the `late` modifier, the `!` operator,
  `required` parameters, and changes to core libraries.

- **[Migrate to null safety](docs/migrate.md)**

  A step-by-step guide for migrating an existing Dart package to null safety.
  Includes instructions for using the `dart migrate` tool,
  checking dependency readiness, and publishing migrated packages.

- **[Frequently asked questions](docs/faq.md)**

  Practical answers to common questions that arise during migration,
  based on experience migrating Google internal code and Dart team packages.
  Covers topics like `late` vs nullable fields, `required` vs `@required`,
  `built_value` classes, `List` constructors, and compilation to JS.

- **[Unsound null safety](docs/unsound.md)**

  Explains mixed-version programs where some libraries are
  null safe and others aren't.
  Covers the differences between sound and unsound null safety,
  how to migrate incrementally, and how to test mixed-version programs.
  Note that Dart 3 requires all code to be fully null safe.

## Credit and license

This content has been reuploaded to this repository with
adjustments and fixes for archival purposes.
It was originally hosted on [dart.dev][] and its
copyright belongs to the Dart project authors.

Except as otherwise noted,
the content in this repository is licensed under a
[Creative Commons Attribution 4.0 International License][cca-4],
and code samples are licensed under the
[3-Clause BSD License][3-bsd] as outlined in the [LICENSE][] file.

[dart.dev]: https://dart.dev
[cca-4]: https://creativecommons.org/licenses/by/4.0/
[3-bsd]: https://opensource.org/license/BSD-3-Clause
[LICENSE]: LICENSE
