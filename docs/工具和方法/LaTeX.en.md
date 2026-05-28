# LaTeX

## Why use LaTeX

During university, you'll inevitably need to write lab reports, course papers, and thesis documents. If you're still using Word for typesetting, you may encounter these frustrations:

- Tedious formula editing, poor formatting
- Messy reference management
- Spending excessive time adjusting formatting
- Format errors during collaboration

LaTeX is a typesetting system widely used in academia, excelling at mathematical formulas, references, and complex layouts. Almost all top CS conferences and journals (IEEE, ACM) require LaTeX submissions.

**Professional mathematical typesetting**

LaTeX's mathematical typesetting is its greatest strength. Whether it's simple fractions, integrals, or complex matrices and equations, LaTeX produces beautiful results.

**Automated reference management**

With BibTeX and LaTeX, citation and formatting of references is fully automated — no more manual adjustments.

**Consistent formatting**

LaTeX is template-based. As long as the content is correct, the formatting will be correct. No more manual adjustments to fonts, line spacing, or margins.

**Standard for academic writing**

CS academic papers are almost exclusively written in LaTeX. Learning LaTeX early benefits future research work.

## Getting started

**Using Overleaf (recommended for beginners)**

[Overleaf](https://www.overleaf.com/) is an online LaTeX editor. No installation needed — just open a browser.

1. Register an Overleaf account
2. Choose a template (e.g., IEEE Conference, Article, etc.)
3. Edit directly in the browser with real-time preview

**Local installation**

For local use, TeX Live (cross-platform) or MiKTeX (Windows) is recommended:

```bash
# Windows (via Scoop)
scoop install texlive

# macOS
brew install --cask mactex

# Linux (Ubuntu)
sudo apt install texlive-full
```

For local editing, VS Code with the LaTeX Workshop extension is recommended.

## Basic syntax

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage[utf8]{inputenc}

\title{My First LaTeX Document}
\author{Author Name}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}
This is a document written in LaTeX.

\section{Mathematical Formulas}
Inline formula: $E = mc^2$

Display formula:
\begin{equation}
    f(x) = \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
\end{equation}

\end{document}
```

## Common commands cheat sheet

**Document structure**

```latex
\section{Heading 1}
\subsection{Heading 2}
\subsubsection{Heading 3}
```

**Math formulas**

```latex
$x_i$          # Subscript
$x^n$          # Superscript
$\frac{a}{b}$  # Fraction
$\sum_{i=1}^{n}$  # Summation
$\int_{a}^{b}$    # Integral
```

**Lists**

```latex
\begin{itemize}
    \item First item
    \item Second item
\end{itemize}
```

**Inserting images**

```latex
\usepackage{graphicx}
\includegraphics[width=0.8\textwidth]{image.png}
```

## Other resources

- [Overleaf Official Tutorials](https://www.overleaf.com/learn)
- [The Not So Short Introduction to LaTeX2e](https://tobi.oetiker.ch/lshort/lshort.pdf) — classic LaTeX introduction
- [LaTeX Formula Editor](https://www.codecogs.com/latex/eqneditor.php) — online formula editor
- [TeX Stack Exchange](https://tex.stackexchange.com/) — LaTeX Q&A community
