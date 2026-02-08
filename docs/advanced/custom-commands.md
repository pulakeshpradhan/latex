# Custom Commands

LaTeX allows you to define your own commands to simplify complex tasks or enforce consistency.

## Defining a New Command

Use `\newcommand` to create a new command. This is useful for abbreviations or commonly used phrases.

```latex
\newcommand{\R}{\mathbb{R}} % New command "R"
The real numbers are denoted by $\R$.
```

## Adding Arguments

You can create commands that take arguments. The number of arguments is specified in `[]` (up to 9). Use `#1`, `#2`, etc. to refer to them.

```latex
\newcommand{\boldtext}[1]{\textbf{#1}}

This is \boldtext{important}.
```

## Example: Complex Math Command

Instead of typing `\frac{\partial f}{\partial x}` repeatedly:

```latex
\newcommand{\pd}[2]{\frac{\partial #1}{\partial #2}}

The derivative is $\pd{f}{x}$.
```

## Optional Arguments

The first argument can be optional.

```latex
\newcommand{\plusbinomial}[3][2]{(#2 + #3)^#1}

Default (power 2): $\plusbinomial{x}{y}$ % (x+y)^2
Power 3:           $\plusbinomial[3]{x}{y}$ % (x+y)^3
```

## Renewing Commands (`\renewcommand`)

If a command already exists (like `\emph` or `\section`), use `\renewcommand` to change its definition.

```latex
\renewcommand{\abstractname}{Executive Summary}
```

## Defining Environments

Use `\newenvironment{name}{begin code}{end code}`.

```latex
\newenvironment{king}
    {\rule{1ex}{1ex}%
     \hspace{\stretch{1}}}
    {\hspace{\stretch{1}}%
     \rule{1ex}{1ex}}
```
