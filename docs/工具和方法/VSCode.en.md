# VS Code

## Why choose VS Code

While learning CS, you need a capable code editor. Although Vim is essential keyboard operation skills, you still need a feature-rich IDE for daily development. VS Code is currently the most popular code editor, balancing lightweight design with powerful features.

**Free and open source**

VS Code is completely free, maintained by Microsoft, with an active community and frequent updates.

**Rich extension ecosystem**

VS Code has a massive extension library covering virtually every programming language and development scenario. Python, C/C++, Java, JavaScript, LaTeX, Docker — all have dedicated extensions.

**Built-in Git support**

VS Code has built-in Git integration, allowing you to commit, manage branches, and resolve conflicts through a graphical interface — very friendly for beginners.

**Remote development**

Through extensions like Remote - SSH and Remote - Containers, VS Code can connect directly to remote servers or Docker containers for development with a smooth local-like experience.

## Installing VS Code

**Windows**

Download from the [VS Code website](https://code.visualstudio.com/), or use Scoop:

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

## Recommended extensions

**Programming languages**

- **Python** — essential for Python development (by Microsoft)
- **C/C++** — C/C++ development support (by Microsoft)
- **Java Extension Pack** — complete Java development toolkit
- **JavaScript (ES6) code snippets** — JavaScript code snippets

**Productivity tools**

- **Vim** — use Vim keybindings in VS Code
- **GitLens** — enhanced Git features, view code history and blame
- **Error Lens** — display error messages inline in code
- **Todo Tree** — highlight and manage TODO comments in code

**Remote development**

- **Remote - SSH** — connect to remote servers for development
- **Remote - Containers** — develop inside Docker containers
- **WSL** — develop in WSL

**Other recommendations**

- **LaTeX Workshop** — LaTeX editing support
- **Docker** — Docker management
- **Thunder Client** — API testing tool
- **indent-rainbow** — indentation visualization

## Useful tips

**Command Palette**

Press `Ctrl+Shift+P` (`Cmd+Shift+P` on macOS) to open the command palette, where you can search and execute any command.

**Multi-cursor editing**

Hold `Alt` and click at multiple locations to edit multiple places simultaneously.

**Quick file open**

Press `Ctrl+P` (`Cmd+P` on macOS) and type a filename to quickly open files.

**Sidebar minimap**

Add to `settings.json`:

```json
{
    "editor.minimap.enabled": true,
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

## Other resources

- [VS Code Official Documentation](https://code.visualstudio.com/docs)
- [VS Code Keybinding Reference](https://code.visualstudio.com/docs/getstarted/keybindings)
- [Awesome VS Code](https://github.com/viatsko/awesome-vscode) — extensions and resource collection
