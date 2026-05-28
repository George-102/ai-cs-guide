# Git

## 为什么使用 Git

在学习计算机科学的过程中，你会不断地写代码、做项目、参与协作。如果没有版本控制，你很可能会遇到以下情况：

- 代码改坏了无法恢复
- 多人协作时文件互相覆盖
- 不记得某个功能是什么时候加的、为什么加的

Git 是目前世界上最流行的分布式版本控制系统，几乎所有开源项目和企业开发都在使用它。掌握 Git 不仅是开发必备技能，也是参与开源社区、找工作的敲门砖。

**版本控制，永不丢失**

Git 会记录你每一次代码变更的历史。你可以随时回退到任意一个历史版本，不用担心改坏代码。

**分支管理，安全试错**

Git 的分支机制让你可以在不影响主代码的情况下尝试新功能。合并失败了？没关系，分支随时可以丢弃。

**协作必备，开源基石**

GitHub、GitLab 等平台都基于 Git。参与开源项目、提交 Pull Request、Code Review，这些都离不开 Git。

## 安装 Git

**Windows**

推荐使用 Scoop 安装：

```powershell
scoop install git
```

或者从 [Git 官网](https://git-scm.com/download/win) 下载安装包。

**macOS**

```bash
brew install git
```

**Linux（Ubuntu/Debian）**

```bash
sudo apt update
sudo apt install git
```

安装完成后，配置你的身份信息：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

## 怎么学习 Git

Git 的命令看似繁多，但日常开发中常用的只有几个。推荐的学习路线：

1. 阅读 [廖雪峰的 Git 教程](https://liaoxuefeng.com/books/git/index.html)，中文讲解非常清晰
2. 阅读 [Pro Git](https://git-scm.com/book/zh/v2) 电子书，这是最权威的 Git 学习资料
3. 在实际项目中使用 Git，边用边学是最高效的方式

**常用 Git 命令速查**

```bash
git init                  # 初始化仓库
git clone <url>           # 克隆远程仓库
git add .                 # 暂存所有更改
git commit -m "消息"      # 提交更改
git push                  # 推送到远程
git pull                  # 拉取远程更新
git branch <name>         # 创建分支
git checkout <name>       # 切换分支
git merge <name>          # 合并分支
git log                   # 查看提交历史
```

## GitHub

Git 是版本控制工具，GitHub 是基于 Git 的代码托管平台。几乎所有知名开源项目都在 GitHub 上托管。

**基本工作流程**

1. 在 GitHub 上创建仓库（Repository）
2. `git clone` 克隆到本地
3. 编写代码，`git add` + `git commit` 提交
4. `git push` 推送到 GitHub
5. 发起 Pull Request 参与协作

**建议**

- 尽早建立自己的 GitHub 主页，持续积累项目
- 多参与开源项目的 Issue 和 Pull Request
- 善用 GitHub Actions 实现自动化工作流

## 其他资源

- [Git 官方文档](https://git-scm.com/doc)
- [GitHub 官方教程](https://docs.github.com)
- [Git 可视化学习](https://learngitbranching.js.org/?locale=zh_CN)
- [Oh Shit, Git!?!](https://ohshitgit.com/zh) — Git 常见错误的急救指南
