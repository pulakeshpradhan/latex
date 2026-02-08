# Tables

Tables in LaTeX can be tricky at first. The basic environment is `tabular`.

## Basic Table Structure

```latex
\begin{tabular}{c c c}
  A & B & C \\
  1 & 2 & 3 \\
  4 & 5 & 6 \\
\end{tabular}
```

- `{c c c}`: Defines three columns, all centered.
  - `l`: Left-aligned column.
  - `r`: Right-aligned column.
  - `c`: Center-aligned column.
  - `|`: Vertical line separator (e.g., `{l|c|r}`).

- `&`: Separates cells in a row.
- `\\`: Ends a row.
- `\hline`: Draws a horizontal line across the table.

## Example with Lines

```latex
\begin{tabular}{|l|c|r|}
  \hline
  \textbf{Item} & \textbf{Qty} & \textbf{Price} \\
  \hline
  Apples & 5 & \$1.00 \\
  Oranges & 10 & \$2.00 \\
  \hline
\end{tabular}
```

## Floating Tables (`table` Environment)

To make a table "float" (LaTeX decides the best position) and add a caption, wrap `tabular` in `table`.

```latex
\begin{table}[h]
    \centering
    \begin{tabular}{l c r}
        \hline
        Task & Duration & Status \\
        \hline
        Design & 2w & Done \\
        Code & 4w & In Progress \\
        Test & 2w & Pending \\
        \hline
    \end{tabular}
    \caption{Project Timeline}
    \label{tab:project}
\end{table}
```

- `[h]`: Try to place the table *here*. (Options: `h`ere, `t`op, `b`ottom, `p`age).
- `\centering`: Centers the table.
- `\caption{...}`: Adds a descriptive title.
- `\label{...}`: Use this to reference the table (`Table \ref{tab:project}`).

## Professional Tables (`booktabs`)

For publication-quality tables, use the `booktabs` package (`\usepackage{booktabs}`). It provides better spacing and cleaner lines.

- `\toprule`: Top line (thick).
- `\midrule`: Middle line (thin).
- `\bottomrule`: Bottom line (thick).

```latex
\begin{table}[ht]
    \centering
    \begin{tabular}{@{}llr@{}} \toprule
        \multicolumn{2}{c}{Item} \\ \cmidrule(r){1-2}
        Animal & Description & Price (\$)\\ \midrule
        Gnat  & per gram & 13.65 \\
        & each     & 0.01 \\
        Gnu   & stuffed  & 92.50 \\
        Emu   & stuffed  & 33.33 \\
        Armadillo & frozen & 8.99 \\ \bottomrule
    \end{tabular}
    \caption{A nice table with booktabs}
\end{table}
```
