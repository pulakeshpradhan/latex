# Document Structure

Understanding how LaTeX structures documents is key to efficient writing.

## The Preamble

The preamble (before `\begin{document}`) defines everything about your document before the content starts:

- **Load `\documentclass`**: The type of document you are creating (article, report, book, letter).
- **Load `\usepackage`**: Any external packages you need (graphics, math, bibliography).
- **Set Up Metadata**: Title, author, date (`\title{...}`, `\author{...}`, `\date{...}`).
- **Define Formatting**: Font size (`10pt`, `11pt`, `12pt`), language (`[english]`), paper size (`[a4paper]`).

Example Preamble:

```latex
\documentclass[12pt, a4paper]{article}
\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{amsmath}

\title{My Research Paper}
\author{John Doe}
\date{\today}
```

## Classes

| Class | Purpose | Structure |
| :--- | :--- | :--- |
| `article` | Short documents without chapters (papers, reports, etc.) | `section`, `subsection`, `subsubsection` |
| `report` | Longer documents with chapters (theses, technical documentation) | `chapter`, `section`, `subsection` |
| `book` | Books (allows frontmatter, mainmatter, backmatter) | `part`, `chapter`, sections... |
| `letter` | Letters | `opening`, `closing` |
| `beamer` | Slides / Presentations | `frame`, `block` |

## Sections and Chapters

LaTeX automatically numbers headings and generates a Table of Contents.

- `\part{...}` (only in Books)
- `\chapter{...}` (only in Reports and Books)
- `\section{...}`
- `\subsection{...}`
- `\subsubsection{...}`
- `\paragraph{...}`
- `\subparagraph{...}`

To create an unnumbered section (but still appear in the text), use the starred version (`*`):
`\section*{Introduction}` (won't be numbered "1. Introduction").

## Table of Contents

Place `\tableofcontents` where you want the TOC to appear. LaTeX generates it automatically based on your section commands. You may need to compile twice for the TOC to update correctly.
To add unnumbered sections to the TOC, use `\addcontentsline{toc}{section}{Introduction}`.

## Lists

### Bulleted Lists (`itemize`)

```latex
\begin{itemize}
    \item First item
    \item Second item
\end{itemize}
```

### Numbered Lists (`enumerate`)

```latex
\begin{enumerate}
    \item First item
    \item Second item
\end{enumerate}
```

### Description Lists (`description`)

```latex
\begin{description}
    \item[First] The first definition.
    \item[Second] The second definition.
\end{description}
```
