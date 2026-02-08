# Lists

Lists are fundamental for structuring content. LaTeX supports bulleted (`itemize`), numbered (`enumerate`), and description (`description`) lists.

## Standard Lists

### Bullet Points (`itemize`)

```latex
\begin{itemize}
    \item Apples
    \item Oranges
    \item Bananas
\end{itemize}
```

### Numbered List (`enumerate`)

```latex
\begin{enumerate}
    \item Introduction
    \item Methods
    \item Results
\end{enumerate}
```

### Descriptions (`description`)

```latex
\begin{description}
    \item[HTML] HyperText Markup Language
    \item[CSS] Cascading Style Sheets
\end{description}
```

## Nested Lists

You can nest lists up to 4 levels deep.

```latex
\begin{enumerate}
    \item Fruit
    \begin{itemize}
        \item Apple
        \item Banana
    \end{itemize}
    \item Vegetables
    \begin{itemize}
        \item Carrot
        \item Potato
    \end{itemize}
\end{enumerate}
```

## Customizing Lists (The `enumitem` Package)

To customize list styles (e.g., replace bullets with dashes, change numbering to a), b)), use the `enumitem` package.

Add to preamble: `\usepackage{enumitem}`.

### Custom Bullets

```latex
\begin{itemize}[label=$\star$]
    \item Star item 1
    \item Star item 2
\end{itemize}
```

### Custom Numbering

- `label=\alph*` -> a, b, c
- `label=\Alph*` -> A, B, C
- `label=\roman*` -> i, ii, iii
- `label=\Roman*` -> I, II, III
- `label=\arabic*` -> 1, 2, 3

```latex
\begin{enumerate}[label=(\alph*)]
    \item First item (a)
    \item Second item (b)
\end{enumerate}
```

### Spacing

Remove vertical space between items using `nosep` or adjust `itemsep`.

```latex
\begin{itemize}[nosep]
    \item Compact Item 1
    \item Compact Item 2
\end{itemize}
```
