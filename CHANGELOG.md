# Changelog

## 1.0.0

**Release date:** TBD

Version 1.0.0 is the first release of `term`.

- Added the `term` package.
  - `term.width`: Returns the number of terminal columns that text takes.
  - `term.strip_ansi`: Removes every ANSI escape sequence from text.
  - `term.wrap`: Wraps text to a width in columns and keeps its colors across line breaks.
  - `term.truncate`: Shortens text to a width in columns and ends it with an ellipsis.
  - `term.pad`: Pads text with spaces to a width in columns.
  - `term.table`: Draws rows of cells as a table.
  - `term.box`: Draws a box around text.
  - `term.spinner`: Returns a one-line indicator of work in progress.
  - `term.progress`: Returns a progress bar for a known amount of work.
