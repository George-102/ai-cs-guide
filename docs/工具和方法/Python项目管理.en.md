# Python Project Management

## Why do you need project management tools

When you first start writing Python, you might just `pip install` everything into the system Python. But soon you will run into these problems:

- Project A needs `requests==2.28`, project B needs `requests==2.31` — version conflicts
- You switch to a different machine and nothing runs because you forgot which packages you installed
- The system Python gets messy and is hard to clean up

The core problems Python project management tools solve are: **environment isolation** and **dependency locking**. Below are four commonly used tools and when to use each.

## pip — Package Installer

pip is Python's built-in package manager, responsible for downloading and installing third-party libraries from [PyPI](https://pypi.org/).

```bash
# Install a package
pip install requests

# Install a specific version
pip install requests==2.31.0

# Upgrade a package
pip install --upgrade requests

# Uninstall a package
pip uninstall requests

# List installed packages
pip list

# Export all dependencies in the current environment
pip freeze > requirements.txt

# Install all dependencies from requirements.txt
pip install -r requirements.txt
```

> **Note:** Never `pip install` directly into the system Python — this pollutes the global environment. Always use a virtual environment.

## venv — Built-in Virtual Environments

venv is a built-in module in Python 3.3+ for creating virtual environments. It creates an isolated Python environment for each project, avoiding package version conflicts.

**Creating a virtual environment**

```bash
# Create a virtual environment in the project directory
python -m venv .venv
```

**Activation and usage**

```bash
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

# Windows (cmd)
.venv\Scripts\activate.bat

# macOS / Linux
source .venv/bin/activate

# After activation, (.venv) appears at the beginning of your prompt
(.venv) $ pip install requests
(.venv) $ python main.py

# Deactivate the virtual environment
deactivate
```

**Typical workflow**

```bash
# 1. Create project and initialize virtual environment
mkdir myproject && cd myproject
python -m venv .venv

# 2. Activate environment
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\Activate.ps1  # Windows

# 3. Install dependencies
pip install flask sqlalchemy

# 4. Lock dependencies
pip freeze > requirements.txt

# 5. Commit requirements.txt to Git, add .venv to .gitignore
echo ".venv/" >> .gitignore
```

**`.gitignore` configuration**

```
# .gitignore
.venv/
__pycache__/
*.pyc
```

> **Tip:** Naming your virtual environment `.venv` (with a dot prefix) is a community convention that many tools recognize automatically.

## Poetry — Modern Dependency Management

[Poetry](https://python-poetry.org/) is a tool that combines dependency management, virtual environments, and package publishing. It replaces `setup.py`, `requirements.txt`, `setup.cfg`, and other config files with a single `pyproject.toml`.

**Installing Poetry**

```bash
# Windows (PowerShell)
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -

# macOS / Linux
curl -sSL https://install.python-poetry.org | python3 -
```

**Creating a project**

```bash
# New project (generates directory structure and pyproject.toml)
poetry new myproject

# Initialize in an existing project
cd existing-project
poetry init
```

**Dependency management**

```bash
# Add a dependency (automatically updates pyproject.toml and poetry.lock)
poetry add requests
poetry add flask sqlalchemy

# Add a dev dependency (only used during development, not published)
poetry add --group dev pytest black

# Remove a dependency
poetry remove requests

# Install all dependencies (exact restore from poetry.lock)
poetry install

# Update dependencies
poetry update
```

**Running the project**

```bash
# Run a command in the virtual environment
poetry run python main.py
poetry run pytest

# Or activate the virtual environment first
poetry shell
python main.py
```

**`pyproject.toml` example**

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

| Feature | pip + venv | Poetry |
|---------|-----------|--------|
| Dependency resolution | Manual | Automatic conflict resolution |
| Lock file | `requirements.txt` (manual freeze) | `poetry.lock` (auto-generated) |
| Virtual environment | Manual creation and activation | Auto-managed |
| Package publishing | Requires setup.py + twine | `poetry build && poetry publish` |
| Config files | Multiple (requirements.txt, setup.py...) | Single `pyproject.toml` |

## pyenv — Python Version Management

[pyenv](https://github.com/pyenv/pyenv) lets you install and switch between multiple Python versions on the same machine. Different projects may need different Python versions — pyenv makes this simple.

**Installing pyenv**

```bash
# macOS (Homebrew)
brew install pyenv

# Linux (automatic install script)
curl https://pyenv.run | bash

# Add the following to ~/.bashrc or ~/.zshrc
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
```

> **Windows users:** Use [pyenv-win](https://github.com/pyenv-win/pyenv-win):
> ```powershell
> pip install pyenv-win --target $HOME/.pyenv
> ```

**Basic usage**

```bash
# List available Python versions
pyenv install --list

# Install a specific version
pyenv install 3.11.7
pyenv install 3.12.2

# List installed versions
pyenv versions

# Set the global default version
pyenv global 3.11.7

# Set the version for the current project (run in the project directory)
pyenv local 3.12.2

# Check the current version
pyenv version
```

**Project-level Python version**

```bash
cd myproject
pyenv local 3.11.7
# Creates a .python-version file in the project directory
# Running python in this directory will now use 3.11.7 automatically
```

## Recommended Tool Combinations

Choose the right combination based on project size:

**Beginner / small scripts: pip + venv**

```bash
python -m venv .venv
source .venv/bin/activate
pip install requests
pip freeze > requirements.txt
```

Sufficient, zero dependencies, built into Python.

**Medium to large projects: Poetry**

```bash
poetry init
poetry add flask sqlalchemy pytest
poetry run python main.py
```

Automatic dependency resolution, lock file, one-command publishing.

**Multiple Python versions: pyenv + Poetry**

```bash
pyenv install 3.11.7
pyenv install 3.12.2
pyenv local 3.11.7
poetry init
poetry add requests
```

Precise Python version control + modern dependency management.

## FAQ

**`pip install` gives a permission error?**

Never use `sudo pip install` — this pollutes the system Python. Make sure the virtual environment is activated first, then install.

**What is the difference between `requirements.txt` and `poetry.lock`?**

- `requirements.txt` is the output of `pip freeze`, listing all packages with exact versions, but does not distinguish direct from transitive dependencies
- `poetry.lock` is auto-generated by Poetry, recording exact versions and hashes for every package to ensure reproducible builds

**pyenv fails to compile Python?**

Install build dependencies:

```bash
# Ubuntu / Debian
sudo apt install build-essential libssl-dev zlib1g-dev \
  libbz2-dev libreadline-dev libsqlite3-dev libffi-dev

# macOS
xcode-select --install
```

## Other Resources

- [pip Official Documentation](https://pip.pypa.io/en/stable/)
- [venv Official Documentation](https://docs.python.org/3/library/venv.html)
- [Poetry Official Documentation](https://python-poetry.org/docs/)
- [pyenv GitHub](https://github.com/pyenv/pyenv)
- [Python Packaging User Guide](https://packaging.python.org/) — The authoritative guide to Python packaging
