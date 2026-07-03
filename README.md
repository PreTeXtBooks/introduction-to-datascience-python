## Data Science: A First Introduction

This is the source for the PreTeXt version of *Data Science: A First Introduction in Python* textbook.

The original book is available online at: https://python.datasciencebook.ca

© 2020 Tiffany A. Timbers, Trevor Campbell, Melissa Lee

For the R version of the textbook, please visit https://datasciencebook.ca or the PreTeXt version at https://github.com/PreTeXtBooks/introduction-to-datascience/

## License Information

This textbook is offered under
the [Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Development

This book is built with [PreTeXt](https://pretextbook.org/), an XML-based authoring language for open-source textbooks. The PreTeXt project lives in the `pretext/` directory, with the chapter source files under `pretext/source/`.

### Setup

Building the book requires the `pretext` command-line tool. Install it with:
```
pip install pretext
```
See the [PreTeXt CLI installation guide](https://pretextbook.org/doc/guide/html/getting-started-installation.html) for more details, including any additional dependencies needed for PDF output (a LaTeX distribution) or other formats.

### Build locally

From the `pretext/` directory, build the HTML version of the book by running
```
cd pretext
pretext build web
```
You can then view the built book in your browser with
```
pretext view web
```

To build the PDF version of the book, run
```
pretext build print
```
in the `pretext/` directory. The generated PDF will be placed in `pretext/output/print/`.

### Project structure

- `pretext/project.ptx` - overall PreTeXt project configuration (defines the `web`/`print` build targets)
- `pretext/source/main.ptx` - main book file, which assembles the chapters
- `pretext/source/ch_*.ptx` - individual chapter source files
- `pretext/publication/` - publication configuration (styling/output options)
- `pretext/assets/` - static assets (images, data files, etc.) referenced by the source
- `pretext/output/` - generated build output (not tracked in git)

### Contributing

Primary development in this repository happens on the `main` branch. If you want to contribute to the book,
please branch off of `main` and make a pull request into `main`. You cannot commit directly to `main`.

## Style Guide

### General
- **80 character line limit!** This is necessary to make git diffs useful
- numbers in text should be english words ("four common mistakes" not "4 common mistakes") unless there are units (40km, not forty km)
- use Oxford commas ("a, b, and c" not "a, b and c")
- "subset" should not be used as a verb
- functions in text should not have parentheses (`read_csv` not `read_csv()`)
- remove all references to "course" and "student"; replace with "reader" or "you" where necessary
- make sure we have permission to use all external resources that we use
- remove all references to "clicking on things" in the HTML version of the book (e.g. "click this link to ...")
- When we introduce a new term, use `**bolding**` to typeset it (but only the first introduction of the term)
- for symbols as part of the text, make sure you give them their full name and surround with parentheses so that they
  don't "disappear" in the rest of the text. So for example, if I have a `,` in the text, I should do
  something like  "here is some text about the comma (`,`)". Or for `<-`, we should do "something like this assignment operator (`<-`)".
  There are likely exceptions to this rule though.
- Book titles in the text should be typeset in italics (e.g. *R for Data Science*)
