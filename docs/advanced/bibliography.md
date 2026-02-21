# Bibliography and Citations

LaTeX makes referencing and formatting bibliographies powerful and automatic.

1. **BibTeX**: The classic approach.
2. **BibLaTeX**: The modern, feature-rich replacement.

## 1. BibTeX

### Creating a Database (`.bib` file)

Create a file like `references.bib` and add entries:

```bibtex
@article{einstein1905,
    author  = "Albert Einstein",
    title   = "{Zur Elektrodynamik bewegter K{\"o}rper}. ({German})
               [{On} the electrodynamics of moving bodies]",
    journal = "Annalen der Physik",
    volume  = "322",
    number  = "10",
    pages   = "891--921",
    year    = "1905",
    doi     = "http://dx.doi.org/10.1002/andp.19053221004"
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

Einstein's theory of relativity \cite{einstein1905} revolutionized physics.
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

## 3. In-Text Citation Commands

Modern packages like `biblatex` and `natbib` provide specific commands for different citation styles.

### BibLaTeX Citation Table

| Command | Description | Output (**authoryear**) | Output (**numeric**) |
| :--- | :--- | :--- | :--- |
| `\cite{key}` | Basic citation | Einstein 1905 | [1] |
| `\parencite{key}` | In parentheses | (Einstein, 1905) | [1] |
| `\textcite{key}` | Narrative (author in text) | Einstein (1905) | Einstein [1] |
| `\autocite{key}` | Context-sensitive | (Einstein, 1905) | [1] |
| `\footcite{key}` | Citation in footnote | Citation in footer | ¹ |
| `\citeauthor{key}` | Author name only | Einstein | Einstein |
| `\citeyear{key}` | Year only | 1905 | 1905 |
| `\nocite{key}` | Add to bib without citing | (No output) | (No output) |

> 🌟 **Pro Tip: Style Independence with `\autocite`**
> Use `\autocite{key}` instead of `\cite` or `\parencite`. It is context-sensitive and adapts to the style defined in your preamble.
>
> - If you switch between **APA**, **MLA**, or **Chicago** (footnotes), `\autocite` automatically adjusts the formatting (e.g., converting to footnotes or changing parentheses) without you having to manually edit your text!

### Natbib Equivalence Table

If you are using the `natbib` package, use these commands:

| Natbib Command | BibLaTeX Equivalent | Purpose | Example |
| :--- | :--- | :--- | :--- |
| `\citet{key}` | `\textcite{key}` | Narrative citation | Einstein (1905) |
| `\citep{key}` | `\parencite{key}` | Parenthetical citation | (Einstein, 1905) |
| `\citet*{key}` | N/A | Full author list | Einstein, Podolsky, & Rosen (1935) |

### Practical Usage Example

Here is how you might use these commands in a research paper:

**LaTeX Source:**

```latex
In the field of physics, \textcite{einstein1905} introduced the revolutionary 
concept of special relativity. This work remains a cornerstone of modern 
science \parencite{einstein1905}. Later, developers like \citeauthor{knuth1984} 
focused on the presentation of such ideas through software, specifically in 
his work during \citeyear{knuth1984}. General guides such as \autocite{latexcompanion} 
provide further technical depth. For more info, see the project docs \footcite{mkdocs}.
```

**Rendered Output (Author-Year):**
> In the field of physics, **Einstein (1905)** introduced the revolutionary concept of special relativity. This work remains a cornerstone of modern science **(Einstein, 1905)**. Later, developers like **Knuth** focused on the presentation of such ideas through software, specifically in his work during **1984**. General guides such as **(Goossens et al., 1993)** provide further technical depth. For more info, see the project docs **¹**.

### Author Variations (Single, Two, 3+)

How citations look depends on the number of authors in the `.bib` entry:

| Author Count | Example `author` field | `\textcite` Output | `\parencite` Output |
| :--- | :--- | :--- | :--- |
| **1 Author** | `Albert Einstein` | Einstein (1905) | (Einstein, 1905) |
| **2 Authors** | `Jane Doe and John Smith` | Doe and Smith (2024) | (Doe and Smith, 2024) |
| **3+ Authors** | `Alice Alpha and Bob Beta and others` | Alpha et al. (2025) | (Alpha et al., 2025) |

> 👋 **Note**: The use of "et al." for 3 or more authors is automatic in styles like `authoryear` or `apa`.

---

## Natbib (Alternative)

Often used in sciences for author-year citations (`\citep`, `\citet`). Compatible with BibTeX styles.

```latex
\usepackage{natbib}
\bibliographystyle{plainnat}
```

## 4. Troubleshooting: "Not Reflecting"

If your citations or bibliography are not appearing:

1. **Check Compilation Order**:
    - For **BibTeX**: `pdflatex` → `bibtex` → `pdflatex` → `pdflatex`.
    - For **BibLaTeX**: `pdflatex` → `biber` → `pdflatex`.
2. **Verify File Names**: Ensure `\bibliography{filename}` or `\addbibresource{filename.bib}` exactly matches your `.bib` file name.
3. **Check Keys**: Ensure the key in `\cite{key}` exactly matches the key in the `@entry{key, ...}` in your `.bib` file.
4. **Auxiliary Files**: Sometimes old `.aux` or `.bbl` files cause issues. Try deleting them and re-compiling.
