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
