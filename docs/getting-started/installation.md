# Getting Started with LaTeX

Before we write our first document, we need to install a LaTeX distribution and an editor.

## Step 1: Install a LaTeX Distribution

A LaTeX **distribution** provides all the tools and packages needed to process your LaTeX code and produce PDF documents.

### Windows

- **[MiKTeX](https://miktex.org/download)**: A popular, lightweight distribution. It installs packages on-the-fly as you need them.
- **[TeX Live](https://tug.org/texlive/)**: A comprehensive distribution (large download) covering everything.

**Recommendation:** Go with **MiKTeX** if you have limited space, or **TeX Live** for a complete setup.

### macOS

- **[MacTeX](https://www.tug.org/mactex/)**: Based on TeX Live, this is the standard distribution for macOS. It includes TeXShop and other utilities.

### Linux

Most Linux distributions manage TeX Live through their package managers:

```bash
sudo apt-get install texlive-full  # Debian/Ubuntu (Note: lengthy install!)
sudo dnf install texlive-scheme-full # Fedora
```

### Online Alternative (No Installation)

If you prefer not to install software, use **[Overleaf](https://www.overleaf.com/)**. It's a powerful online LaTeX editor with real-time collaboration and cloud storage. Perfect for beginners!

## Step 2: Choose an Editor

A specialized LaTeX editor makes writing code much easier with syntax highlighting and auto-completion.

1. **[Visual Studio Code](https://code.visualstudio.com/)**: The most popular code editor today. Install the **LaTeX Workshop** extension by James Yu. It is powerful and customizable.
2. **TeXShop** (macOS only): Simple and effective, comes with MacTeX.
3. **TeXworks / TeXstudio**: Dedicated LaTeX IDEs with many built-in features.

**Recommendation:** **VS Code + LaTeX Workshop** for a modern experience.
