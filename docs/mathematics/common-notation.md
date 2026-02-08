# Common Mathematical Notation

The `amsmath`, `amssymb`, and `amsfonts` packages are essential.

## Superscripts & Subscripts

- Superscripts: `^`
  - $x^2$ - `x^2`
  - $e^{-x}$ - `e^{-x}` (Note: multiple characters must be in `{}`)
  - $2^{3x+1}$ - `2^{3x+1}`

- Subscripts: `_`
  - $a_n$ - `a_n`
  - $x_{i,j}$ - `x_{i,j}`
  - $H_2O$ - `H_2O`

- Combined
  - $x_i^2$ - `x_i^2`

## Greek Letters

| Lowercase | Command | Uppercase | Command |
| :--- | :--- | :--- | :--- |
| $\alpha$ | `\alpha` | $A$ | `A` |
| $\beta$ | `\beta` | $B$ | `B` |
| $\gamma$ | `\gamma` | $\Gamma$ | `\Gamma` |
| $\delta$ | `\delta` | $\Delta$ | `\Delta` |
| $\epsilon$ | `\epsilon` | $E$ | `E` |
| $\zeta$ | `\zeta` | $Z$ | `Z` |
| $\eta$ | `\eta` | $H$ | `H` |
| $\theta$ | `\theta` | $\Theta$ | `\Theta` |
| $\iota$ | `\iota` | $I$ | `I` |
| $\kappa$ | `\kappa` | $K$ | `K` |
| $\lambda$ | `\lambda` | $\Lambda$ | `\Lambda` |
| $\mu$ | `\mu` | $M$ | `M` |
| $\nu$ | `\nu` | $N$ | `N` |
| $\xi$ | `\xi` | $\Xi$ | `\Xi` |
| $\pi$ | `\pi` | $\Pi$ | `\Pi` |
| $\rho$ | `\rho` | $P$ | `P` |
| $\sigma$ | `\sigma` | $\Sigma$ | `\Sigma` |
| $\tau$ | `\tau` | $T$ | `T` |
| $\upsilon$ | `\upsilon` | $\Upsilon$ | `\Upsilon` |
| $\phi$ | `\phi` | $\Phi$ | `\Phi` |
| $\chi$ | `\chi` | $X$ | `X` |
| $\psi$ | `\psi` | $\Psi$ | `\Psi` |
| $\omega$ | `\omega` | $\Omega$ | `\Omega` |

## Operators

- Summation: `\sum_{i=1}^n` $\sum_{i=1}^n$
- Integral: `\int_a^b` $\int_a^b$
- Limit: `\lim_{x \to \infty}` $\lim_{x \to \infty}$
- Product: `\prod` $\prod$

## Brackets and Parentheses

Scale automatically with `\left` and `\right`.

- `\left( \frac{1}{2} \right)` $\rightarrow \left( \frac{1}{2} \right)$
- `\left[ ... \right]`
- `\left\{ ... \right\}` (Use `\{` for braces)
- `\left| ... \right|` (Absolute value)
- `\left\langle ... \right\rangle` (Angle brackets)

## Sets

- $\in$ `\in`
- $\notin$ `\notin`
- $\subset$ `\subset`
- $\subseteq$ `\subseteq`
- $\cup$ `\cup`
- $\cap$ `\cap`
- $\emptyset$ `\emptyset`
- $\infty$ `\infty`
- $\mathbb{R}$ `\mathbb{R}` (Real numbers - `amsfonts`)
- $\mathbb{Z}$ `\mathbb{Z}` (Integers)
- $\mathbb{N}$ `\mathbb{N}` (Natural numbers)
- $\mathbb{C}$ `\mathbb{C}` (Complex numbers)

## Text in Math Mode

Inside math mode, spaces are ignored. Use `\text{...}` to write normal text.
`text{if } x > 0` $\rightarrow \text{if } x > 0$
