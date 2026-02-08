# Inline vs Display Math

Math is LaTeX's super power. There are two primary modes for typesetting mathematics:

## 1. Inline Mode (`$...$`)

Use inline mode to mix mathematical symbols within the flow of text.
For example, writing `$E=mc^2$` produces $E=mc^2$ right here.

### Syntax

- Wrap your math expression in single dollar signs: `$ ... $`
- Alternatively, use `\( ... \)` (LaTeX standard).

**Example:**
The equation for a line is $y = mx + b$, where $m$ is the slope and $b$ is the y-intercept.

## 2. Display Mode (`\[...\]` or `$$...$$`)

Display mode centers the equation on its own line and uses larger symbols for readability.
For example:
$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$

### Syntax

- **Unnumbered Equation**: Use `\[ ... \]` (recommended) or `$$ ... $$` (TeX primitive, often used but less robust).
- **Numbered Equation**: Use the `equation` environment for automatic numbering.

**Example (Numbered):**

```latex
\begin{equation}
    x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
    \label{eq:quadratic}
\end{equation}
```

This will produce a centered equation with a number like (1) on the right side. You can reference it later using `\ref{eq:quadratic}`.

## Aligning Equations

For multi-line equations, use the `align` environment (requires `amsmath` package). alignment points are marked with `&`.

```latex
\begin{align}
    f(x) &= (x+1)^2 \\
         &= x^2 + 2x + 1
\end{align}
```

The `\\` creates a new line. The `&` aligns the equals signs.

To suppress numbering for specific lines, use `\nonumber` or switch to `align*`.
