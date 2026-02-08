# Brackets, Matrices, and Arrays

## Brackets

Scale brackets automatically using `\left` and `\right`.

### Parentheses `( )`

$$ \left( \frac{1}{2} \right) $$
`\left( ... \right)`

### Square Brackets `[ ]`

$$ \left[ \begin{matrix} 1 & 0 \\ 0 & 1 \end{matrix} \right] $$
`\left[ ... \right]`

### Curly Braces `{ }`

$$ \left\{ x \in \mathbb{R} \mid x > 0 \right\} $$
`\left\{ ... \right\}` (Must escape `\{`!)

### Absolute Value `| |`

$$ \left| -5 \right| = 5 $$
`\left| ... \right|`

### Angle Brackets `< >`

$$ \langle u, v \rangle $$
`\langle ... \rangle` or `\left\langle ... \right\rangle`

## Matrices and Arrays

Requires `amsmath`. Standard environments:

- `matrix`: No brackets.
- `pmatrix`: Parentheses `( )`.
- `bmatrix`: Square brackets `[ ]`.
- `Bmatrix`: Curly braces `{ }`.
- `vmatrix`: Single bars `| |` (determinant).
- `Vmatrix`: Double bars `|| ||` (norm).

The structure is similar to a table:

- Rows are separated by `\\`.
- Columns are separated by `&`.

### Examples

**pmatrix**:
$$ \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} $$

```latex
\begin{pmatrix}
  1 & 2 \\
  3 & 4
\end{pmatrix}
```

**bmatrix**:
$$ \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix} $$

```latex
\begin{bmatrix}
  1 & 2 & 3 \\
  4 & 5 & 6 \\
  7 & 8 & 9
\end{bmatrix}
```

## Creating Cases Functions

Use the `cases` environment for piecewise functions.

$$ f(x) = \begin{cases} 2x & x > 0 \\ 0 & x \le 0 \end{cases} $$

```latex
f(x) = \begin{cases}
  2x & x > 0 \\
  0 & x \le 0
\end{cases}
```
