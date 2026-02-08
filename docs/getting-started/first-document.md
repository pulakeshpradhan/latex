# Your First LaTeX Document

Let's create our first LaTeX file and understand the basic anatomy of a document.

## Creating a File

Create a new file called `hello-world.tex` (or use the example file `00_Creating_a_LaTeX_Document.tex` from this guide).

Type the following code:

```latex title="hello-world.tex"
\documentclass[12pt]{article}
\usepackage{amsmath, amssymb, amsfonts}

\title{My First Document}
\author{Your Name}
\date{\today}

\begin{document}

\maketitle

Hello! This is my first \LaTeX\ document.

A rectangle has side lengths of $(x+1)$ and $(x+3)$.
The equation $A(x) = x^2+4x+3$ gives the area of the rectangle.

\end{document}
```

## Compilation

To turn this into a PDF, you need to **compile** it. In VS Code with LaTeX Workshop, simply save the file (`Ctrl+S`).
The output should look like a formatted document with the title, author (you), and today's date, followed by your text.

## Understanding the Structure

Every LaTeX document has two main parts:

### 1. Preamble (Before `\begin{document}`)

The preamble sets up the document.

- `\documentclass{article}`: Defines the document type (article, report, book, letter). The `[12pt]` option sets the base font size.
- `\usepackage{...}`: Loads external packages to add functionality (like `amsmath` for math support).
- `\title{...}`, `\author{...}`: Metadata commands.

### 2. Body (`\begin{mcdocument} ... \end{document}`)

The actual content of your document goes here. Everything outside this environment is ignored or part of the preamble.

- `\maketitle`: Prints the title, author, and date.
- `$...$`: Inline math mode.
- `\LaTeX`: A command that prints the LaTeX logo.

## Common Errors

- Mismatched `\begin{...}` and `\end{...}`.
- Forgetting `\usepackage{...}` for a command (e.g. using `\frac` without `amsmath` sometimes works but best practice is to load it).
- Using special characters like `%`, `$`, `&`, `_`, `{`, `}`, `#` without escaping them (e.g. `\%`).

## Next Steps

Now you have a basic document structure. Let's learn how to format text in the next section.
