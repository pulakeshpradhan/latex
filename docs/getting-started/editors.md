# Choosing an Editor

A specialized LaTeX editor makes writing code much easier with syntax highlighting, auto-completion, and integrated PDF viewing.

## 1. Visual Studio Code (Cross-Platform)

**Highly Recommended**

VS Code is a powerful, extensible code editor. When combined with the **LaTeX Workshop** extension, it provides a top-tier LaTeX experience.

### Features

- **Intellisense**: Autocompletion (commands, labels, bibtex keys).
- **Structure View**: Outline of sections/chapters for easy navigation.
- **SyncTeX**: Click in PDF -> jump to code. Ctrl+Click in code -> jump to PDF.
- **Linting**: Errors/warnings shown inline as you type (ChkTeX).
- **Snippets**: Expand common patterns (e.g., `fig` -> complete figure environment).

### Installation

1. Install [VS Code](https://code.visualstudio.com/).
2. Open Extensions (Ctrl+Shift+X).
3. Search for "LaTeX Workshop" (by James Yu).
4. Install.

## 2. Overleaf (Online)

**Best for Collaboration**

Overleaf is a cloud-based LaTeX editor. It requires no installation and allows real-time collaboration (like Google Docs).

### Pros

- **Zero Setup**: Just sign up and start writing.
- **Collaboration**: Multiple users can edit simultaneously.
- **Rich Text Mode**: "Word-like" editing for beginners.
- **Templates**: Thousands of templates (journals, CVs, theses).

### Cons

- **Offline Access**: Limited (requires paid plan/git sync).
- **Compile Time**: Can be slow on free tier for large documents.

## 3. Dedicated Editors

These specific applications are designed purely for LaTeX.

### TeXstudio (Windows/Mac/Linux)

A feature-rich IDE. It has many buttons and menus to insert symbols, making it very beginner-friendly if you don't know commands by heart.

- **Wizards**: For tables, arrays, newly created documents.
- **Symbol Panel**: 1000+ symbols accessible via click.

### TeXShop (macOS only)

Simple, clean, and reliable. Comes with MacTeX. It focuses on the source and preview without clutter.

### TeXworks

Minimalist editor often included with MiKTeX/TeX Live. Good for simple edits but lacks advanced features like structure view or strict autocompletion.

## Recommendation

- New to coding? Start with **Overleaf**.
- Want a powerful local setup? Use **VS Code + LaTeX Workshop**.
