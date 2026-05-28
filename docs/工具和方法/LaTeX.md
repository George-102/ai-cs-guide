# LaTeX

## 为什么使用 LaTeX

在大学学习中，你不可避免地需要写实验报告、课程论文、毕业设计文档。如果你还在用 Word 排版，可能会遇到以下困扰：

- 公式编辑繁琐，排版不美观
- 参考文献管理混乱
- 格式调整耗费大量时间
- 多人协作时格式容易出错

LaTeX 是学术界广泛使用的排版系统，特别擅长处理数学公式、参考文献和复杂排版。几乎所有计算机领域的顶级会议和期刊（如 IEEE、ACM）都要求使用 LaTeX 格式投稿。

**专业的数学公式排版**

LaTeX 的数学公式排版是其最大的优势。无论是简单的分数、积分，还是复杂的矩阵、方程组，LaTeX 都能排版得非常美观。

**自动化的参考文献管理**

使用 BibTeX 配合 LaTeX，参考文献的引用和格式化完全自动化，再也不用手动调整引用格式。

**格式一致性**

LaTeX 基于模板排版，只要内容正确，格式就一定正确。不再需要手动调整字体、行距、页边距。

**学术写作标配**

CS 领域的学术论文几乎都使用 LaTeX 撰写。提前学会 LaTeX，对未来的科研工作大有裨益。

## 入门方式

**使用 Overleaf（推荐新手）**

[Overleaf](https://www.overleaf.com/) 是一个在线 LaTeX 编辑器，无需安装任何软件，打开浏览器就能使用。

1. 注册 Overleaf 账号
2. 选择一个模板（如 IEEE Conference、Article 等）
3. 直接在网页上编辑，实时预览效果

**本地安装**

如果你想在本地使用 LaTeX，推荐安装 TeX Live（跨平台）或 MiKTeX（Windows）：

```bash
# Windows（使用 Scoop）
scoop install texlive

# macOS
brew install --cask mactex

# Linux（Ubuntu）
sudo apt install texlive-full
```

本地编辑器推荐使用 VS Code + LaTeX Workshop 插件。

## 基本语法

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage[utf8]{inputenc}

\title{我的第一篇 LaTeX 文档}
\author{作者名}
\date{\today}

\begin{document}

\maketitle

\section{简介}
这是一篇用 LaTeX 撰写的文档。

\section{数学公式}
行内公式：$E = mc^2$

行间公式：
\begin{equation}
    f(x) = \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
\end{equation}

\end{document}
```

## 常用命令速查

**文档结构**

```latex
\section{一级标题}
\subsection{二级标题}
\subsubsection{三级标题}
```

**数学公式**

```latex
$x_i$          # 下标
$x^n$          # 上标
$\frac{a}{b}$  # 分数
$\sum_{i=1}^{n}$  # 求和
$\int_{a}^{b}$    # 积分
```

**列表**

```latex
\begin{itemize}
    \item 第一项
    \item 第二项
\end{itemize}
```

**插入图片**

```latex
\usepackage{graphicx}
\includegraphics[width=0.8\textwidth]{image.png}
```

## 其他资源

- [Overleaf 官方教程](https://www.overleaf.com/learn)
- [一份不太简短的 LaTeX2e 介绍](https://github.com/CTeX-org/lshort-zh-cn) — 中文 LaTeX 入门经典
- [LaTeX 公式编辑器](https://www.codecogs.com/latex/eqneditor.php) — 在线公式编辑
- [TeX Stack Exchange](https://tex.stackexchange.com/) — LaTeX 问答社区
