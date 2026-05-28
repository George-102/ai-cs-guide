# Obsidian

## 为什么使用 Obsidian

学习 CS 的过程中，你会接触大量概念、笔记、代码片段和学习资源。如果只是把它们分散在各种文档和文件夹里，时间一长就会混乱不堪。Obsidian 是一款基于 Markdown 的笔记工具，特别适合整理和关联知识。

**纯本地存储，数据安全**

Obsidian 的笔记就是本地的 `.md` 文件，不依赖任何云服务。你的数据完全在自己手里，不会因为平台关闭而丢失。

**双向链接，构建知识网络**

Obsidian 的核心功能是双向链接。你可以通过 `[[]]` 语法将笔记互相引用，形成知识图谱，帮助你发现知识点之间的关联。

**Markdown 原生支持**

所有笔记都是标准的 Markdown 文件，和你的 MkDocs 站点、GitHub README 等完全兼容。

**丰富的插件生态**

社区插件非常丰富：日历、看板、Excalidraw（手绘白板）、Dataview（数据查询）等，几乎能满足所有需求。

## 安装 Obsidian

从 [Obsidian 官网](https://obsidian.md/) 下载安装，支持 Windows、macOS、Linux、iOS、Android。

## 基本使用

**创建 Vault（仓库）**

首次打开 Obsidian 时会提示你创建或打开一个 Vault。Vault 就是一个普通的文件夹，Obsidian 会在其中管理你的笔记。

**创建笔记**

- 点击左侧的「新建笔记」按钮
- 或者按 `Ctrl+N`（macOS: `Cmd+N`）

**双向链接**

在笔记中输入 `[` 然后输入另一篇笔记的标题，即可创建链接：

```markdown
# 数据结构

参见 [[算法导论]] 中的排序算法章节。
```

被链接的笔记会自动显示反向链接，让你知道哪些笔记引用了它。

**标签**

使用 `#` 给笔记打标签，方便分类：

```markdown
#操作系统 #进程 #并发
```

**文件夹组织**

可以按课程或主题组织文件夹结构：

```
Vault/
├── 00-Inbox/          # 临时笔记
├── 01-CS基础/
│   ├── 数据结构/
│   ├── 操作系统/
│   └── 计算机网络/
├── 02-AI/
│   ├── 机器学习/
│   └── 深度学习/
└── Templates/         # 模板
```

## 推荐插件

- **Calendar** — 日历视图，方便管理每日笔记
- **Templater** — 高级模板功能
- **Dataview** — 用 SQL-like 语法查询笔记
- **Excalidraw** — 在笔记中嵌入手绘白板
- **Kanban** — 看板视图，管理任务和项目
- **Git** — 自动同步笔记到 GitHub

## 其他资源

- [Obsidian 官网](https://obsidian.md/)
- [Obsidian 官方帮助文档](https://help.obsidian.md/)
- [Obsidian 中文社区](https://forum.obsidian.md/c/chinese/50)
- [Linking Your Thinking](https://www.linkingyourthinking.com/) — Obsidian 使用方法论
