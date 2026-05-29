# Python 项目管理

## 为什么需要项目管理工具

刚开始写 Python 时，你可能直接 `pip install` 一切，所有包装在系统 Python 里。但很快你会遇到这些问题：

- 项目 A 需要 `requests==2.28`，项目 B 需要 `requests==2.31`，版本冲突
- 换一台电脑，跑不起来了，忘了当初装了哪些包
- 系统 Python 被搞乱，卸载不干净

Python 项目管理工具解决的核心问题就是：**隔离环境**和**锁定依赖**。下面介绍四个常用工具及其适用场景。

## pip — 包安装器

pip 是 Python 自带的包管理器，负责从 [PyPI](https://pypi.org/) 下载和安装第三方库。

```bash
# 安装包
pip install requests

# 安装指定版本
pip install requests==2.31.0

# 升级包
pip install --upgrade requests

# 卸载包
pip uninstall requests

# 查看已安装的包
pip list

# 导出当前环境的所有依赖
pip freeze > requirements.txt

# 从 requirements.txt 安装所有依赖
pip install -r requirements.txt
```

> **注意：** 永远不要在系统 Python 里直接 `pip install`，这会污染全局环境。配合虚拟环境使用才是正确姿势。

## venv — 内置虚拟环境

venv 是 Python 3.3+ 内置的虚拟环境模块，无需额外安装。它为每个项目创建独立的 Python 环境，避免包之间的版本冲突。

**创建虚拟环境**

```bash
# 在项目目录下创建虚拟环境
python -m venv .venv
```

**激活和使用**

```bash
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Windows (cmd)
.venv\Scripts\activate.bat

# macOS / Linux
source .venv/bin/activate

# 激活后命令行前会出现 (.venv) 标识
(.venv) $ pip install requests
(.venv) $ python main.py

# 退出虚拟环境
deactivate
```

**典型工作流**

```bash
# 1. 创建项目并初始化虚拟环境
mkdir myproject && cd myproject
python -m venv .venv

# 2. 激活环境
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\Activate.ps1  # Windows

# 3. 安装依赖
pip install flask sqlalchemy

# 4. 锁定依赖
pip freeze > requirements.txt

# 5. 提交 requirements.txt 到 Git，.venv 目录加入 .gitignore
echo ".venv/" >> .gitignore
```

**`.gitignore` 配置**

```
# .gitignore
.venv/
__pycache__/
*.pyc
```

> **提示：** 推荐将虚拟环境命名为 `.venv`（带点前缀），这是社区惯例，很多工具会自动识别。

## Poetry — 现代化依赖管理

[Poetry](https://python-poetry.org/) 是一个集依赖管理、虚拟环境、打包发布于一体的工具。它用 `pyproject.toml` 替代了 `setup.py`、`requirements.txt`、`setup.cfg` 等多个配置文件。

**安装 Poetry**

```bash
# Windows (PowerShell)
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -

# macOS / Linux
curl -sSL https://install.python-poetry.org | python3 -
```

**创建项目**

```bash
# 新建项目（自动生成目录结构和 pyproject.toml）
poetry new myproject

# 在已有项目中初始化
cd existing-project
poetry init
```

**依赖管理**

```bash
# 添加依赖（自动更新 pyproject.toml 和 poetry.lock）
poetry add requests
poetry add flask sqlalchemy

# 添加开发依赖（仅在开发时使用，不会打包发布）
poetry add --group dev pytest black

# 移除依赖
poetry remove requests

# 安装所有依赖（根据 poetry.lock 精确还原）
poetry install

# 更新依赖
poetry update
```

**运行项目**

```bash
# 在虚拟环境中运行命令
poetry run python main.py
poetry run pytest

# 或者先激活虚拟环境
poetry shell
python main.py
```

**`pyproject.toml` 示例**

```toml
[tool.poetry]
name = "myproject"
version = "0.1.0"
description = "My awesome project"
authors = ["Your Name <you@example.com>"]

[tool.poetry.dependencies]
python = "^3.10"
requests = "^2.31"
flask = "^3.0"

[tool.poetry.group.dev.dependencies]
pytest = "^8.0"
black = "^24.0"

[build-system]
requires = ["poetry-core"]
build-backend = "poetry.core.masonry.api"
```

**Poetry vs pip + venv**

| 特性 | pip + venv | Poetry |
|------|-----------|--------|
| 依赖解析 | 手动管理 | 自动解析冲突 |
| 锁定文件 | `requirements.txt`（手动 freeze） | `poetry.lock`（自动生成） |
| 虚拟环境 | 手动创建激活 | 自动管理 |
| 包发布 | 需要 setup.py + twine | `poetry build && poetry publish` |
| 配置文件 | 多个（requirements.txt, setup.py...） | 单个 `pyproject.toml` |

## pyenv — Python 版本管理

[pyenv](https://github.com/pyenv/pyenv) 让你在同一台机器上安装和切换多个 Python 版本。不同项目可能需要不同的 Python 版本，pyenv 让这一切变得简单。

**安装 pyenv**

```bash
# macOS (Homebrew)
brew install pyenv

# Linux (自动安装脚本)
curl https://pyenv.run | bash

# 将以下内容添加到 ~/.bashrc 或 ~/.zshrc
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
```

> **Windows 用户：** 使用 [pyenv-win](https://github.com/pyenv-win/pyenv-win)：
> ```powershell
> pip install pyenv-win --target $HOME/.pyenv
> ```

**基本使用**

```bash
# 查看可安装的 Python 版本
pyenv install --list

# 安装指定版本
pyenv install 3.11.7
pyenv install 3.12.2

# 查看已安装的版本
pyenv versions

# 设置全局默认版本
pyenv global 3.11.7

# 为当前项目设置版本（在项目目录下执行）
pyenv local 3.12.2

# 查看当前使用的版本
pyenv version
```

**项目级 Python 版本**

```bash
cd myproject
pyenv local 3.11.7
# 会在项目目录下生成 .python-version 文件
# 之后在该目录下运行 python 会自动使用 3.11.7
```

## 工具组合推荐

根据项目规模选择合适的工具组合：

**入门 / 小型脚本：pip + venv**

```bash
python -m venv .venv
source .venv/bin/activate
pip install requests
pip freeze > requirements.txt
```

够用、零依赖、Python 内置。

**中大型项目：Poetry**

```bash
poetry init
poetry add flask sqlalchemy pytest
poetry run python main.py
```

自动依赖解析、锁定文件、一键发布。

**多 Python 版本共存：pyenv + Poetry**

```bash
pyenv install 3.11.7
pyenv install 3.12.2
pyenv local 3.11.7
poetry init
poetry add requests
```

精确控制 Python 版本 + 现代化依赖管理。

## 常见问题

**`pip install` 报权限错误怎么办？**

不要用 `sudo pip install`，这会污染系统 Python。先确认已激活虚拟环境，再安装。

**`requirements.txt` 和 `poetry.lock` 有什么区别？**

- `requirements.txt` 是 `pip freeze` 的输出，列出所有包及其精确版本，但不区分直接依赖和间接依赖
- `poetry.lock` 由 Poetry 自动生成，记录每个包的精确版本和哈希值，确保可复现构建

**pyenv 安装 Python 编译失败？**

安装编译依赖：

```bash
# Ubuntu / Debian
sudo apt install build-essential libssl-dev zlib1g-dev \
  libbz2-dev libreadline-dev libsqlite3-dev libffi-dev

# macOS
xcode-select --install
```

## 其他资源

- [pip 官方文档](https://pip.pypa.io/en/stable/)
- [venv 官方文档](https://docs.python.org/3/library/venv.html)
- [Poetry 官方文档](https://python-poetry.org/docs/)
- [pyenv GitHub](https://github.com/pyenv/pyenv)
- [Python Packaging User Guide](https://packaging.python.org/) — Python 打包生态的权威指南
