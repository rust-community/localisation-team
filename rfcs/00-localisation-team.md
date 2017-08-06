# pre-RFC: Rust Localisation Team

## Summary

This proposal describes the creation of a dedicated
internationalization and  localisation team for the Rust Project. The
team coordinates efforts to implement and maintain l10n and i18n in
the core tools and documentation, but also fosters collaboration
across the ecosystem to provide Rust developers with first level
crates and tools to manage l10n and i18n in their projects.

## Motivation

Rust should be accessible to anyone, no matter their language, place
of birth or race. In order to do this, the Rust project should provide
resources, tools and libraries that people can consume in their own
language to implement localised and/or multi-language products.

This targets a two fold need, an internal one and an external one. In
one side, core tools and documentation should give feedback to users
in their own language. rustc, cargo and rustup, for example, should
provide help and messages in multiple languages according to the
standards of each platform. In the other side, the crate ecosystem
should provide first level crates to manage internationalization and
localisation in projects, i.e., date formatting, translations, rtl,
unicode support, etc.

## Guide-level Explanation

Due to the nature and breadth of its goals, the localisation team work
needs certain hierarchies to be in place. Those hierarchies are
defined as _Special Interest Groups_ and _Language Sub-teams_. 

### Team Goals

- Orchestrate Rust Content internationalization
  - `std` documentation and the Rust Book
  - Videos subtitling and translation
  - Blog posts and Websites' copy
- Implement and maintain internationalization and localization in the
  core tools 
  - `rustc`: error and warning messages, the command line help
  - `std`: provide core functionality to allow internationalization of strings
  - `cargo`: command line help, string extraction tools
  - `rustdoc`: support translation of API docs
  - `mdBook`: support multilingual books
  - `rustup`: command line help
- Support community efforts to implement internationalization and
  localisation libraries in the crate ecosystem.
  - Unicode
  - L20N
  - gettext

### Specific Interest Groups

The special interest groups, or _SIGs_ are topic oriented and
collaborate around a specific team goal. In many case, they work
together with other _upstream_ teams to define and execute tasks. Each
_SIG_ defines its projects and collaboration methods and tools to be used
to execute them.

The proposed _SIGs_ are:

- Documentation
- Videos
- Web
- Core
- Libraries

### Language Sub-teams

The language sub-teams are comprised of people able to collaborate
towards the translation from English to a second language. The
sub-teams can have members of different _SIGs_ and use the tools they
provide to execute the translation of strings.

The language sub-teams collaborate around one or several online
platforms (TBD) to track progress and updates to translations.

## Reference-level Explanation

## Drawbacks

## Rationale and Alternatives

## Unresolved Questions
