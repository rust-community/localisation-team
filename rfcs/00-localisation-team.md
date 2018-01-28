# Localisation Team Pre-RFC

# Pre-RFC: Rust Localisation Team

- Feature Name: Rust Localiation Team
- Start Date: 2018-01-28
- RFC PR: 
- Rust Issue: 

## Summary

Incorporate a Community Project Sub-team dedicated to internationalization
(i18n) and localisation (l10n) for the Rust project. The sub-team will
coordinate with the other Rust teams to implement and maintain i18n
and l10n support in the core tools and documentation. Furthermore, it
will foster collaboration across the ecosystem to provide Rust
developers with high quality crates and tools to manage i18n and l10n
in their project.

## Motivation

The vast majority of Rust tooling and documentation is in English.
Considering outreach and inclusiveness as a core tenet of the
project, Rust should be accessible to anyone, no matter their
language, place of birth or race. In order to make this a reality,
the Rust project should provide resources, tools and libraries that
people can consume in their own language and implement localised
and/or multi-language products.

This RFC targets a two-fold need. First, the tools and documentation
produced by the [Rust Teams](https://www.rust-lang.org/en-US/team.html)
should provide interfaces and give feedback to users in their own
language. rustc, cargo, and rustup, for example, should provide help
and error messages in different languages according to the standards
of each platform. Second, the external crate ecosystem should provide
high quality crates to manage internationalization and localization
in projects, i.e., date formatting, translations, right-to-left
scripts, unicode support, etc.

## Guide-level Explanation

Due to the nature and breadth of its goals, the localisation
subteam work will need to be distributed across several smaller
strike teams. Also, to ease the communication and coordination of
tasks, the sub-teams can be Language specific.

### Team Goals

- Coordinate and execute Rust Content internationalization
  - `std` documentation and the Rust Book
  - Official Videos subtitling and translation
  - Blog posts and Websites' copy
- Provide support for communication in multiple languages across the official discussion forums (Discourse, IRC)
- Implement and maintain internationalization and localization in the core tools
  - `rustc`: error and warning messages, the command line help
  - `std`: provide core functionality to allow internationalization of strings
  - `cargo`: command line help, string extraction tools
  - `rustdoc`: support multilingual API/crate docs
  - `rustup`: command line help, website.
- Support community efforts to implement internationalization and localisation libraries in the crate ecosystem.
  - Unicode: a lot of work done at [rust-unic](https://github.com/behnam/rust-unic)
  - `[mdBook](https://github.com/azerupi/mdBook)`: support multilingual books
  - [L](http://l20n.org/)[2](http://l20n.org/)[0N](http://l20n.org/) (see [rust-lang/rfcs/#822](https://github.com/rust-lang/rfcs/issues/822))
  - [gettext](https://en.wikipedia.org/wiki/Gettext) (see [gettext](https://crates.io/crates/gettext) and [gettext-rs](https://crates.io/crates/gettext-rs))


### Strike Teams

The _Strike Teams_ can assemble to tackle tasks specific to one of the
team goals or topics over a defined timeframe or continuously. The
strike teams are not necessarily comprised of members of the
localisation team and can reach out to community volunteers for
collaboration. Each _Strike Team_ operates autonomously in terms of
the methods and tools used to achieve its goals.

Some examples of Strike Teams are:

- Documentation: localisation of [*the book*](https://doc.rust-lang.org/book/) and `std` documentation
- Videos: subtitling and translation of subtitles of videos the [Rust Videos](https://youtube.com/rustvideos) channel on the [Amara](https://amara.org/) platform
- Moderation: moderation and support of language specific categories or channels in [URLO](https://users.rust-lang.org) and IRC
- Web: translation of official blog posts and websites
- Core: support for l10n/i18n in the core tools and translation of help, warnings and error messages
- Libraries: foster support for l10n/i18n in the crate ecosystem. Infrastructure support for libraries i18n

### Language Sub-teams

The language sub-teams are comprised of people able to collaborate
towards the translation of content from English to a second
language. The sub-teams collaborate with the strike teams and use the
tools they provide to execute the translation of strings.

The language sub-teams collaborate around one or several online
platforms, defined in conjunction with the strike teams to track
progress and manage updates to the translations.

The work of the language sub-teams must be compatible with the
internationalization facilities available in the different tools. For
example, L20N or gettext for software projects or the mechanisms
provided by `mdBook` and `rustdoc` for guides, books and crates
documentation. 


## Reference-level Explanation

The details of the internationalization and localisation process vary
across each project. These should be discussed and agreed on each
_Strike Team_ and the _upstream_ of each project. The definition of
each project’s process is recommended to be done by creating new RFCs
for each project where applicable.

Please refer to [the projects folder] to check out initial proposals
and more detailed guides for how this could work in each case.

[the projects folder]: https://github.com/rust-community/localisation/projects

## Drawbacks

Tackling localisation efforts is not a simple task. It requires a lot
of coordination and dedication, at least initially, to get the process
going in the many different fronts that could benefit from this
work. Automation and tooling is one of the main initial tasks as it
would allow each member of the different *Strike Teams* or *Sub-teams*
to work efficiently and the projects’ *upstream* to integrate this work
easily.

## Rationale and Alternatives

Alternatively, each project could coordinate its own localisation
efforts independently. However, this could represent duplication of
efforts and the implementation of conflicting solutions across the
tools, as well as making it difficult to track the progress and status
of the different initiatives.

**Existing Efforts**

- [The Rust Programming Language translations](https://github.com/rust-lang/book/blob/master/second-edition/src/appendix-06-translation.md)
- [mdBook internationalization support](https://github.com/azerupi/mdBook/issues/5)


## Unresolved Questions

