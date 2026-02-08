# Text Formatting

LaTeX provides robust commands for styling text.

## Font Styles

| Style | Command | Example |
| :--- | :--- | :--- |
| **Bold** | `\textbf{text}` | This is \textbf{bold} text. |
| *Italic* | `\textit{text}` | This is \textit{italic} text. |
| ***Underline*** | `\underline{text}` | This is \underline{underlined} text. |
| `Typewriter` | `\texttt{text}` | This is \texttt{monospaced} text. |
| Small Caps | `\textsc{text}` | This is \textsc{small caps} text. |
| Sans Serif | `\textsf{text}` | This is \textsf{sans serif} text. |
| Roman (Default) | `\textrm{text}` | This is \textrm{serif} text. |

## Combining Styles

You can nest commands: `\textbf{\textit{Bold and Italic}}`.

## Font Sizes

LaTeX has built-in relative font size commands:

| Command | Size | Default 10pt | Default 11pt | Default 12pt |
| :--- | :--- | :--- | :--- | :--- |
| `\tiny` | Tiny | 5pt | 6pt | 6pt |
| `\scriptsize` | Script Size | 7pt | 8pt | 8pt |
| `\footnotesize` | Footnote Size | 8pt | 9pt | 10pt |
| `\small` | Small | 9pt | 10pt | 11pt |
| `\normalsize` | Normal | 10pt | 11pt | 12pt |
| `\large` | Large | 12pt | 12pt | 14pt |
| `\Large` | Larger | 14pt | 14pt | 17pt |
| `\LARGE` | Even Larger | 17pt | 17pt | 20pt |
| `\huge` | Huge | 20pt | 20pt | 25pt |
| `\Huge` | Huge | 25pt | 25pt | 25pt |

Example: `{\Large This text is large.}`

## Alignment

### Left Align (Default)

`\begin{flushleft} ... \end{flushleft}`

### Right Align

`\begin{flushright} ... \end{flushright}`

### Center Align

`\begin{center} ... \end{center}`

## Quotes

Use the `quote` for single paragraphs and `quotation` for multiple paragraphs.

```latex
\begin{quote}
    This is a short quote.
\end{quote}
```

## Creating Space

- `\hspace{1cm}`: Horizontal space.
- `\vspace{1cm}`: Vertical space.
- `\hfill`: Fill remaining horizontal space (pushes text to the right).
- `\vfill`: Fill remaining vertical space (pushes text to the bottom).
- `\newpage`: Start a new page.
