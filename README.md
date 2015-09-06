# Drush Aliases

This is a prototype project with a few goals:

- Replace existing Drush sitealias code with class-based implementation.
- Load aliases from .yml files instead of .drushrc.php files.
- Load and convert legacy .drushrc.php files.
- Provide a reusable library for other systems that might wish to interact with Drush alias files.
- Simplify alias implementation and reduce recursive searching, etc. in order to improve performance, as possible.

The classes do **not** contain any logic to determine where aliases should be loaded from.  These must be supplied by the
caller.

See the examples directory for example alias files.

\Drush\Context\Context:

A key/value store.

\Drush\Context\ContextList:

A prioritized list of contexts.  Also provides accessor functions that will return a matching value from the first context that contains it.

\Drush\Context\Alias:

A \Drush\Context\Context that also contains specific methods particular to aliases.
