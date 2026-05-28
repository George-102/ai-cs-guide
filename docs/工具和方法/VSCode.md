# VS Code

## 为什么选择 VS Code

在学习 CS 的过程中，你需要一个趁手的代码编辑器。虽然 Vim 是必备的键盘操作技能，但在日常开发中，你还需要一个功能丰富的 IDE 来提高效率。VS Code 是目前最流行的代码编辑器，兼具轻量和强大。

**免费且开源**

VS Code 完全免费，由微软维护，社区活跃，更新频繁。

**丰富的扩展生态**

VS Code 拥有海量扩展，覆盖几乎所有编程语言和开发场景。Python、C/C++、Java、JavaScript、LaTeX、Docker 等都有对应的扩展。

**内置 Git 支持**

VS Code 内置了 Git 集成，可以在图形界面中完成提交、分支管理、冲突解决等操作，对新手非常友好。

**远程开发**

通过 Remote - SSH、Remote - Containers 等扩展，VS Code 可以直接连接远程服务器或 Docker 容器进行开发，体验和本地一样流畅。

## 安装 VS Code

**Windows**

从 [VS Code 官网](https://code.visualstudio.com/) 下载安装包，或使用 Scoop：

```powershell
scoop install vscode
```

**macOS**

```bash
brew install --cask visual-studio-code
```

**Linux**

```bash
# Ubuntu/Debian
sudo snap install code --classic
```

## 推荐扩展

**编程语言**

- **Python** — Python 开发必备（Microsoft 出品）
- **C/C++** — C/C++ 开发支持（Microsoft 出品）
- **Java Extension Pack** — Java 开发全套工具
- **JavaScript (ES6) code snippets** — JavaScript 代码片段

**效率工具**

- **Vim** — 在 VS Code 中使用 Vim 键位
- **GitLens** — 增强 Git 功能，查看代码历史和 blame
- **Error Lens** — 在代码行内直接显示错误信息
- **Todo Tree** — 高亮和管理代码中的 TODO 注释

**远程开发**

- **Remote - SSH** — 连接远程服务器开发
- **Remote - Containers** — 在 Docker 容器中开发
- **WSL** — 在 WSL 中开发

**其他推荐**

- **LaTeX Workshop** — LaTeX 编辑支持
- **Docker** — Docker 管理
- **Thunder Client** — API 测试工具
- **indent-rainbow** — 缩进可视化

## 实用技巧

**命令面板**

按 `Ctrl+Shift+P`（macOS: `Cmd+Shift+P`）打开命令面板，可以搜索并执行任何命令。

**多光标编辑**

按住 `Alt` 点击多个位置，可以同时编辑多处代码。

**快速打开文件**

按 `Ctrl+P`（macOS: `Cmd+P`）输入文件名快速打开文件。

**侧边栏缩略图**

在 `settings.json` 中添加：

```json
{
    "editor.minimap.enabled": true,
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

## 其他资源

- [VS Code 官方文档](https://code.visualstudio.com/docs)
- [VS Code 快捷键速查](https://code.visualstudio.com/docs/getstarted/keybindings)
- [Awesome VS Code](https://github.com/viatsko/awesome-vscode) — 扩展和资源汇总
