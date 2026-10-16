# Probability and Computing - Solutions
Probability and Computing (Second Edition). Michael Mitzenmacher, Eli Upfal

This just a fork that aims to publish the pdf version as well.

## Repository layout

```text
solutions.tex                 # Main document and chapter order
preamble.tex                  # Shared packages and formatting
chapters/
  chapter01/
    chapter01.tex             # Chapter title and exercise inputs
    exercises/
      exercise01.01.tex       # Individual exercise solution
      ...
  ...
  chapter08/
```

Each chapter has its own directory. Exercise solutions belong in that chapter's
`exercises/` subdirectory and are included in numerical order by its chapter file.
Chapters without solutions currently contain only their chapter file.

All LaTeX input paths are relative to the repository root. Build from that directory:

```sh
latexmk -pdf solutions.tex
```

To add a solution, create `chapters/chapterNN/exercises/exerciseNN.MM.tex` and add
`\input{chapters/chapterNN/exercises/exerciseNN.MM}` to
`chapters/chapterNN/chapterNN.tex` in numerical order. New chapters must also be
included in `solutions.tex`.
