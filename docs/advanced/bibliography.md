# Bibliography and Citations

LaTeX makes referencing and formatting bibliographies powerful and automatic.

1. **BibTeX**: The classic approach.
2. **BibLaTeX**: The modern, feature-rich replacement.

## 1. BibTeX

### Creating a Database (`.bib` file)

Create a file like `references.bib` and add entries:

```bibtex
@article{einstein,
    author = "Albert Einstein",
    title = "{Zur Elektrodynamik bewegter K{\"o}rper}. ({German})
    [{On} the electrodynamics of moving bodies]",
    journal = "Annalen der Physik",
    volume = "322",
    number = "10",
    pages = "891--921",
    year = "1905",
    DOI = "http://dx.doi.org/10.1002/andp.19053221004"
}

@book{latexcompanion,
    author    = "Michel Goossens and Frank Mittelbach and Alexander Samarin",
    title     = "The \LaTeX\ Companion",
    year      = "1993",
    publisher = "Addison-Wesley",
    address   = "Reading, Massachusetts"
}
```

### In Your Document

Linking the `.bib` file:

```latex
\documentclass{article}

\begin{document}

Einstein's theory of relativity \cite{einstein} revolutionized physics.
The \LaTeX\ Companion \cite{latexcompanion} is an essential book.

\bibliographystyle{plain} % plain, unsrt, alpha, abbrv
\bibliography{references} % filename without .bib

\end{document}
```

### Compilation Order

1. `pdflatex mydoc.tex` (Creates `.aux`)
2. `bibtex mydoc` (Creates `.bbl`)
3. `pdflatex mydoc.tex` (Merges `.bbl`)
4. `pdflatex mydoc.tex` (Updates references)

## 2. BibLaTeX (Recommended)

BibLaTeX is easier to customize and handles complex citations better.

### Preamble setup

```latex
\usepackage[style=authoryear, backend=biber]{biblatex}
\addbibresource{references.bib}
```

- `style=ieee`, `apa`, `mla`, `authoryear`, `numeric`.
- `backend=biber`: Biber is the default engine for BibLaTeX (replace `bibtex` step with `biber`).

### Printing the Bibliography

Place `\printbibliography` where you want the references to appear.

```latex
\printbibliography[heading=bibintoc, title={References}]
```

## Natbib (Alternative)

Often used in sciences for author-year citations (`\citep`, `\citet`). Compatible with BibTeX styles.

```latex
\usepackage{natbib}
\bibliographystyle{plainnat}
```
