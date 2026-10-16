# Probability and Computing - Solutions
Probability and Computing (Second Edition). Michael Mitzenmacher, Eli Upfal

This just a fork that aims to publish the pdf version as well.

## Repository layout

```text
solutions.tex                 # Main document and chapter order
preamble.tex                  # Shared packages and formatting
chapters/
  chapter01/
    chapter01.tex             # Chapter title and exercise solutions
  ...
  chapter08/
```

Each chapter has its own directory. Exercise solutions are written directly in
its chapter file, in numerical order.

All LaTeX input paths are relative to the repository root. Build from that directory:

```sh
latexmk -pdf solutions.tex
```

To add a solution, append a `\paragraph{Exercise N.M}` and its solution to
`chapters/chapterNN/chapterNN.tex` in numerical order. New chapters must also be
included in `solutions.tex`.
