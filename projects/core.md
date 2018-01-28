### Core

The core strike team could focus on adding
internationalization support to the compiler
and core developer tools so they can provide
feedback to users in their own language.

The initial implementation of this work
must be done as a RFC to `rustc`, referencing
and considering previous discussions to add
i18n to the compiler.

A possible starting point of this work, would be
to provide base traits, functions and macros
to allow the internationalization of messages
used by the compiler, in a similar way, and
possibly compatible with, the way `log` works.

One concern to consider for the `rustc`
internationalization is that it should still be
easy to search for feedback and resources regarding
a specific error in the Web. One possible solution
for this, that has been implemented in other projects
like [nodejs] is to add codes to each message or error
type, making it easy to even implement an error code
lookup tool or web service that might be localized as well.

[nodejs]: https://medium.com/the-node-js-collection/node-js-errors-changes-you-need-to-know-about-dc8c82417f65
