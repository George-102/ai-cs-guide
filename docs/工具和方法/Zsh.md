# Oh My Zsh

## 为什么使用 Oh My Zsh

在终端中工作时，你会发现默认的 Bash shell 界面简陋、功能有限。Oh My Zsh 是一个管理 Zsh 配置的框架，让你的终端变得更美观、更高效。

**美观的终端界面**

Oh My Zsh 提供了大量主题，让你的终端支持 Git 分支显示、命令执行时间、彩色提示符等，一目了然。

**强大的自动补全**

Zsh 的自动补全比 Bash 更智能，支持模糊匹配、命令参数提示等，大幅提高输入效率。

**丰富的插件生态**

Oh My Zsh 内置了 300+ 插件，涵盖 Git、Docker、Python、Node.js 等常用工具，让你的终端操作更便捷。

**跨平台支持**

在 macOS、Linux、WSL 上都可以使用 Oh My Zsh。

## 安装 Zsh

**macOS**

macOS 默认可能没有安装 Zsh（虽然新版 macOS 默认 shell 是 Zsh，但版本可能较旧）：

```bash
brew install zsh
```

**Linux**

```bash
sudo apt install zsh
```

**Windows（WSL）**

```bash
sudo apt install zsh
```

**设置 Zsh 为默认 shell**

```bash
chsh -s $(which zsh)
```

> 设置后需要重启终端或注销重新登录才能生效。

## 安装 Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## 推荐配置

**选择主题**

编辑 `~/.zshrc` 文件，修改 `ZSH_THEME`：

```bash
# 推荐主题：agnoster（需要安装字体）
ZSH_THEME="agnoster"

# 或者使用 robbyrussell（Oh My Zsh 默认主题，不需要额外字体）
ZSH_THEME="robbyrussell"
```

> 如果使用 agnoster 主题，需要安装 [Nerd Fonts](https://www.nerdfonts.com/) 字体才能正确显示特殊字符。

**启用常用插件**

编辑 `~/.zshrc` 中的 `plugins` 部分：

```bash
plugins=(
    git                  # Git 命令别名和补全
    docker               # Docker 命令补全
    docker-compose       # Docker Compose 补全
    python               # Python 命令补全
    pip                  # Pip 命令补全
    node                 # Node.js 相关命令
    npm                  # npm 命令补全
    zsh-autosuggestions  # 历史命令自动建议（需额外安装）
    zsh-syntax-highlighting  # 命令语法高亮（需额外安装）
)
```

**安装额外插件**

```bash
# zsh-autosuggestions：输入时自动显示历史命令建议
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# zsh-syntax-highlighting：命令语法实时高亮
git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

安装后重新加载配置：

```bash
source ~/.zshrc
```

## 常用 Git 别名（Oh My Zsh 提供）

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

## 其他资源

- [Oh My Zsh 官网](https://ohmyz.sh/)
- [Oh My Zsh GitHub](https://github.com/ohmyzsh/ohmyzsh)
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
