# Figures and Images

To include images, you need the `graphicx` package: `\usepackage{graphicx}`.

Supported image formats:

- JPEG (`.jpg`)
- PNG (`.png`)
- PDF (`.pdf`) - (Yes, PDFs can be images!)
- EPS (`.eps`)

## Including an Image (`\includegraphics`)

The `\includegraphics{filename}` command inserts an image at the current location.
Always specify its size or scaling.

```latex
\includegraphics[width=0.5\linewidth]{myimage.png}
```

- `width=0.5\linewidth`: Sets the image width to 50% of the text width.
- `width=5cm`: Sets the width to exactly 5 cm.
- `height=2in`: Sets the height to exactly 2 inches.
- `scale=0.8`: Scales the image to 80% of its original size.
- `angle=90`: Rotates the image 90 degrees.

## Floating Figures (`figure` Environment)

Like tables, figures usually float. LaTeX decides where to place them to optimize page breaks.

```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.8\textwidth]{graph.png}
    \caption{A descriptive caption for the graph.}
    \label{fig:mygraph}
\end{figure}
```

- `\centering`: Centers the figure horizontally.
- `[htbp]`: Placement preference:
  - `h`: Here (at this precise location in the code).
  - `t`: Top of a page (default).
  - `b`: Bottom of a page.
  - `p`: Page of floats (all figures together).
  - `!`: Override internal parameters (force harder).
- `\caption`: Adds "Figure 1: ..." text.
- `\label`: Adds an internal reference (e.g., `Reference Figure \ref{fig:mygraph}`).

## Subfigures (`subcaption`)

To place multiple images side-by-side, use the `subcaption` package (`\usepackage{subcaption}`).

```latex
\begin{figure}
    \centering
    \begin{subfigure}[b]{0.45\textwidth}
        \includegraphics[width=\textwidth]{image1}
        \caption{Image A}
    \end{subfigure}
    \hfill
    \begin{subfigure}[b]{0.45\textwidth}
        \includegraphics[width=\textwidth]{image2}
        \caption{Image B}
    \end{subfigure}
    \caption{Two images side-by-side}
\end{figure}
```

## Troubleshooting

- **Image not found?** Ensure the filename and path are correct. Use relative paths (`images/logo.png`) or absolute paths.
- **Image too big?** Use `width=\textwidth` to constrain it to the page width.
- **Figure "floating away"?** This is normal behavior. Use `\clearpage` to force all pending floats to place before continuing.
