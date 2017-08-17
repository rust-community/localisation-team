# Localisation Team Pre-RFC

# Pre-RFC: Rust Localisation Team

- Feature Name: (fill me in with a unique ident, my_awesome_feature)
- Start Date: (fill me in with today's date, YYYY-MM-DD)
- RFC PR: (leave this empty)
- Rust Issue: (leave this empty)

## Summary

This proposal describes the creation of a dedicated
internationalization and localisation working group for the Rust
Project. The team would coordinate efforts to implement and maintain
l10n and i18n in the core tools and documentation. Furthermore, it
would foster collaboration across the ecosystem to provide Rust
developers with high quality crates and tools to manage l10n and i18n
in their projects.

Incorporate a strike team dedicated to internationalization (i18n) and
localisation (l10n) for the Rust project. The strike team will
coordinate with the other Rust subteams to implement and maintain i18n
and l10n support in the core tools and documentation. Furthermore, it
will foster collaboration across the ecosystem to provide Rust
developers with high quality crates and tools to manage i18n and l10n
in their project.

## Motivation

The vast majority of Rust tooling and documentation is in
English. Rust should be accessible to anyone, no matter their
language, place of birth or race. In order to make this a reality, the
Rust project should provide resources, tools and libraries that people
can consume in their own language and implement localised and/or
multi-language products.

This RFC targets a two-fold need. First, the tools and documentation
produced by the [Rust
Teams](https://www.rust-lang.org/en-US/team.html) should give feedback
to users in their own language. rustc, cargo, and rustup, for example,
should provide help and error messages in multiple languages according
to the standards of each platform. Second, the external crate
ecosystem should provide high quality crates to manage
internationalization and localization in projects, i.e., date
formatting, translations, right-to-left scripts, unicode support,
etc.

## Guide-level Explanation

Due to the nature and breadth of its goals, the localisation team work
needs certain hierarchies to be in place. Those hierarchies are
defined as *Strike Teams* and *Localisation Sub-teams*.

### Team Goals

- Orchestrate Rust Content internationalization
  - `std` documentation and the Rust Book
  - Videos subtitling and translation
  - Blog posts and Websites' copy
- Provide support for communication in multiple languages across the official discussion forums (Discourse, IRC)
- Implement and maintain internationalization and localization in the core tools
  - `rustc`: error and warning messages, the command line help
  - `std`: provide core functionality to allow internationalization of strings
  - `cargo`: command line help, string extraction tools
  - `rustdoc`: support translation of API/crate docs
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
_Strike Team_ and the _upstream_ of each project. The high level
process documented here for each project would serve as a starting
point for such discussion. The definition of each project’s process
would be better done by creating new RFCs for each project were
applicable.

### The Rust Programming Language Book

The translation work should focus only on the second edition of the
book.

#### mdBook support

The book internationalization work depends mainly on the level of
support that `mdBook`, the tool used for its development, can give to
*Language Sub-teams*. For this reason, it’s considered high priority
to improve `mdBook` for this goal.

Multiple designs for `mdBook` internationalization support has been
discussed in [its issue
tracker](https://github.com/azerupi/mdBook/issues/5). A strike team
could assemble to define a final design for this and implement it.

With internationalization support in place, the current translation
initiatives should adapt their work to be compatible with it. Each
translation team could create a fork of the book git repository and
add their translated files according to the structure defined by
`mdBook`.

#### Pre-release work

Before the first official release of the second edition, the
translation work should only be done on finished chapters. There
should be a mechanism of notification if changes are done to finished
chapters after translation work has begun on it.

#### Translation teams

The translation teams should have a contact person, who will be
responsible of coordinating efforts, tracking progress, reviewing
translations and releasing chapters as pull requests to the book’s git
repository.

#### Release criteria

The translations can be released on a per-chapter or complete book
manner depending on what the documentation team decides as being
convenient.

#### Chapter freezing

Depending on the process defined by the documentation team for updates
to the book on each Rust release, there could be freeze dates for
translators to work on specific chapters that will not change anymore
for the current release.

#### Translation freezing

Translations should also be frozen an amount of time before a release
sufficient to review, integrate and build them into the final released
book.

### std and crates Documentation

#### rustdoc Support

`rustdoc`, as the official tool to document APIs in Rust, should
provide support for translators to provide alternatives to the
original documentation in different languages.

### Videos

All the videos added to the Rust Videos channel are tracked in the
[Rust sub-project of Mozilla’s Amara
Team](https://amara.org/en/teams/mozilla/videos/?project=rust). Amara
provides a platform to easily subtitle and translate subtitles of
videos, and also has progress tracking capabilities built in. Keeping
the Rust Videos in the Mozilla team at Amara could make it easier to
get help from the Mozilla Video Localisation Team.

Some kind of prioritization criteria should be defined to be able to
reach out to collaborators on the different Language Sub-teams and
focus on the most important videos. This could avoid having people
dedicating time to videos on topics that are already obsolete, for
example. A bulk of videos could be marked for translation and promoted
through the different communication channels.

There should also be constant communication with the Mozilla Video
Localisation Team in order to keep the videos list up to date and to
try to get their collaboration and guidance on the
internationalization work. 

### Moderation

The moderation team could operate independently of the rest of the
strike teams and would not have a defined timeframe for its goals. The
goals of the moderation team is to serve as an umbrella for the
moderators of language specific categories in the Rust Users Forum.

### Web Content

Important publications and relevant content across the different
channels of the project could benefit of being available in different
languages. One example of this could be the anual survey, as well as
roadmap progress reports and announcements.

### Core

The core strike team could focus on adding internationalization
support to the compiler and core developer tools so they can provide
feedback to users in their own language.

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

