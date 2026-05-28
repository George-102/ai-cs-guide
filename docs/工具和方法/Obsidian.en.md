# Obsidian

## Why use Obsidian

While learning CS, you'll encounter a wealth of concepts, notes, code snippets, and learning resources. If scattered across various documents and folders, they'll become chaotic over time. Obsidian is a Markdown-based note-taking tool, especially suited for organizing and connecting knowledge.

**Local storage, data security**

Obsidian notes are local `.md` files, independent of any cloud service. Your data is entirely in your hands and won't be lost if a platform shuts down.

**Bi-directional links, build a knowledge network**

Obsidian's core feature is bi-directional linking. You can reference notes with `[[]]` syntax, forming a knowledge graph that helps you discover connections between concepts.

**Native Markdown support**

All notes are standard Markdown files, fully compatible with your MkDocs site, GitHub README, and more.

**Rich plugin ecosystem**

Community plugins are abundant: Calendar, Kanban, Excalidraw (drawing whiteboard), Dataview (data queries), and more — covering virtually every need.

## Installing Obsidian

Download from the [Obsidian website](https://obsidian.md/). Available on Windows, macOS, Linux, iOS, and Android.

## Basic usage

**Create a Vault**

When you first open Obsidian, you'll be prompted to create or open a Vault. A Vault is just a regular folder where Obsidian manages your notes.

**Create notes**

- Click the "New note" button on the left
- Or press `Ctrl+N` (`Cmd+N` on macOS)

**Bi-directional links**

In a note, type `[` followed by another note's title to create a link:

```markdown
# Data Structures

See the sorting algorithms chapter in [[Introduction to Algorithms]].
```

The linked note will automatically display backlinks, showing you which notes reference it.

**Tags**

Use `#` to tag notes for easy categorization:

```markdown
#operating-system #process #concurrency
```

**Folder organization**

Organize by course or topic:

```
Vault/
├── 00-Inbox/          # Temporary notes
├── 01-CS-Basics/
│   ├── Data-Structures/
│   ├── Operating-Systems/
│   └── Computer-Networks/
├── 02-AI/
│   ├── Machine-Learning/
│   └── Deep-Learning/
└── Templates/         # Templates
```

## Recommended plugins

- **Calendar** — calendar view for managing daily notes
- **Templater** — advanced template features
- **Dataview** — query notes with SQL-like syntax
- **Excalidraw** — embed hand-drawn whiteboards in notes
- **Kanban** — kanban view for task and project management
- **Git** — auto-sync notes to GitHub

## Other resources

- [Obsidian Website](https://obsidian.md/)
- [Obsidian Official Help](https://help.obsidian.md/)
- [Obsidian Forum](https://forum.obsidian.md/)
- [Linking Your Thinking](https://www.linkingyourthinking.com/) — Obsidian methodology
