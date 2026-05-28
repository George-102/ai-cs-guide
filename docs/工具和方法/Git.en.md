# Git

## Why use Git

As you learn computer science, you'll constantly be writing code, working on projects, and collaborating with others. Without version control, you'll likely encounter situations like:

- Breaking your code with no way to restore it
- Files being overwritten during collaboration
- Forgetting when and why a feature was added

Git is the world's most popular distributed version control system. Nearly all open-source projects and enterprise development rely on it. Mastering Git is not only essential for development but also a gateway to open-source communities and job opportunities.

**Version control, never lose work**

Git records every change you make to your code. You can随时 revert to any previous version, so there's no need to worry about breaking your code.

**Branching, safe experimentation**

Git's branching mechanism lets you try new features without affecting the main codebase. Merge failed? No worries — branches can be discarded at any time.

**Essential for collaboration, foundation of open source**

Platforms like GitHub and GitLab are built on Git. Participating in open-source projects, submitting Pull Requests, and Code Reviews all depend on Git.

## Installing Git

**Windows**

Recommended to install via Scoop:

```powershell
scoop install git
```

Or download the installer from the [official Git website](https://git-scm.com/download/win).

**macOS**

```bash
brew install git
```

**Linux (Ubuntu/Debian)**

```bash
sudo apt update
sudo apt install git
```

After installation, configure your identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## How to learn Git

Git commands may seem numerous, but only a few are used daily. Recommended learning path:

1. Read [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials) — excellent interactive guides
2. Read [Pro Git](https://git-scm.com/book/en/v2) — the most authoritative Git learning resource
3. Use Git in actual projects — learning by doing is the most efficient approach

**Common Git commands cheat sheet**

```bash
git init                  # Initialize a repository
git clone <url>           # Clone a remote repository
git add .                 # Stage all changes
git commit -m "message"   # Commit changes
git push                  # Push to remote
git pull                  # Pull from remote
git branch <name>         # Create a branch
git checkout <name>       # Switch branches
git merge <name>          # Merge a branch
git log                   # View commit history
```

## GitHub

Git is the version control tool; GitHub is the code hosting platform built on Git. Nearly all well-known open-source projects are hosted on GitHub.

**Basic workflow**

1. Create a repository on GitHub
2. `git clone` it to your local machine
3. Write code, `git add` + `git commit` to commit
4. `git push` to send to GitHub
5. Open a Pull Request to collaborate

**Suggestions**

- Set up your GitHub profile early and build projects consistently
- Participate in open-source issues and pull requests
- Use GitHub Actions for automation workflows

## Other resources

- [Git Official Documentation](https://git-scm.com/doc)
- [GitHub Official Tutorials](https://docs.github.com)
- [Learn Git Branching](https://learngitbranching.js.org/) — visual and interactive Git learning
- [Oh Shit, Git!?!](https://ohshitgit.com/) — emergency guide for common Git mistakes
