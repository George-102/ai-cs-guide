# Oh My Zsh

## Why use Oh My Zsh

When working in the terminal, you'll find the default Bash shell has a plain interface and limited features. Oh My Zsh is a framework for managing Zsh configuration, making your terminal more beautiful and efficient.

**Beautiful terminal interface**

Oh My Zsh provides many themes with Git branch display, command execution time, colored prompts, and more — all at a glance.

**Powerful auto-completion**

Zsh's auto-completion is smarter than Bash, supporting fuzzy matching, command argument hints, and more, significantly improving input efficiency.

**Rich plugin ecosystem**

Oh My Zsh includes 300+ plugins covering Git, Docker, Python, Node.js, and other common tools, making terminal operations more convenient.

**Cross-platform support**

Oh My Zsh works on macOS, Linux, and WSL.

## Installing Zsh

**macOS**

```bash
brew install zsh
```

**Linux**

```bash
sudo apt install zsh
```

**Windows (WSL)**

```bash
sudo apt install zsh
```

**Set Zsh as default shell**

```bash
chsh -s $(which zsh)
```

> You need to restart the terminal or re-login for changes to take effect.

## Installing Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Recommended setup

**Choose a theme**

Edit `~/.zshrc` and modify `ZSH_THEME`:

```bash
# Recommended theme: agnoster (requires font installation)
ZSH_THEME="agnoster"

# Or use robbyrussell (default, no extra font needed)
ZSH_THEME="robbyrussell"
```

> If using the agnoster theme, you need to install [Nerd Fonts](https://www.nerdfonts.com/) for special characters to display correctly.

**Enable common plugins**

Edit the `plugins` section in `~/.zshrc`:

```bash
plugins=(
    git                  # Git aliases and completion
    docker               # Docker command completion
    docker-compose       # Docker Compose completion
    python               # Python command completion
    pip                  # Pip command completion
    node                 # Node.js related commands
    npm                  # npm command completion
    zsh-autosuggestions  # History command suggestions (requires extra install)
    zsh-syntax-highlighting  # Command syntax highlighting (requires extra install)
)
```

**Install additional plugins**

```bash
# zsh-autosuggestions: show history command suggestions as you type
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# zsh-syntax-highlighting: real-time command syntax highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Reload configuration after installation:

```bash
source ~/.zshrc
```

## Common Git aliases (provided by Oh My Zsh)

```bash
g       # git
gs      # git status
ga      # git add
gc      # git commit
gp      # git push
gl      # git pull
gd      # git diff
gb      # git branch
gco     # git checkout
```

## Other resources

- [Oh My Zsh Official Website](https://ohmyz.sh/)
- [Oh My Zsh GitHub](https://github.com/ohmyzsh/ohmyzsh)
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
