# WSL

## 为什么使用 WSL

很多 CS 课程的实验环境都是 Linux，但大多数同学的电脑是 Windows。虽然可以安装双系统或使用虚拟机，但都有各自的缺点：

- 双系统切换麻烦，不能同时使用 Windows 和 Linux
- 虚拟机占用资源多，性能差
- 有些软件只支持 Linux，Windows 上无法运行

WSL（Windows Subsystem for Linux）让你在 Windows 上直接运行 Linux，无需虚拟机或双系统。它轻量、快速，与 Windows 文件系统无缝集成。

**无需虚拟机，原生运行**

WSL 2 使用真正的 Linux 内核，性能接近原生 Linux，但不需要安装完整的虚拟机。

**无缝集成 Windows**

Linux 和 Windows 文件系统可以互相访问。在 WSL 中可以访问 Windows 的文件（如 `/mnt/c/Users/`），在 Windows 中也可以访问 WSL 的文件。

**开发体验优秀**

VS Code、Docker Desktop 等工具都对 WSL 有良好支持，可以在 WSL 环境中获得与 Linux 几乎一致的开发体验。

**课程实验必备**

很多 CS 课程（如操作系统、计算机网络、数据库）的实验都基于 Linux，WSL 是 Windows 用户完成这些实验的最佳方案。

## 安装 WSL

在 PowerShell（管理员）中执行：

```powershell
# 安装 WSL 2 和默认的 Ubuntu 发行版
wsl --install
```

安装完成后重启电脑，系统会自动安装 Ubuntu。首次启动时需要设置用户名和密码。

**安装指定的发行版**

```powershell
# 查看可用的发行版
wsl --list --online

# 安装指定发行版
wsl --install -d Ubuntu-22.04
```

**设置 WSL 2 为默认版本**

```powershell
wsl --set-default-version 2
```

## 基本使用

**启动 WSL**

```powershell
# 在 PowerShell 中启动默认发行版
wsl

# 启动指定发行版
wsl -d Ubuntu-22.04
```

**在 WSL 中安装软件**

WSL 中的 Ubuntu 可以使用 `apt` 安装软件：

```bash
sudo apt update
sudo apt install build-essential    # 安装 gcc、g++、make
sudo apt install python3 python3-pip
sudo apt install git
```

**访问 Windows 文件**

```bash
# 在 WSL 中访问 Windows 的 C 盘
cd /mnt/c/Users/你的用户名/

# 访问 Windows 的桌面
cd /mnt/c/Users/你的用户名/Desktop/
```

**在 Windows 中访问 WSL 文件**

在文件资源管理器的地址栏输入 `\\wsl$\` 即可访问 WSL 的文件系统。

## 推荐配置

**安装 Windows Terminal**

从 Microsoft Store 安装 [Windows Terminal](https://aka.ms/terminal)，它提供了更好的终端体验，支持多标签页、自定义主题等。

**在 VS Code 中使用 WSL**

安装 VS Code 的 WSL 扩展后，在 WSL 中输入 `code .` 即可用 VS Code 打开当前目录，所有操作都在 WSL 环境中执行。

**配置 Git**

```bash
# 在 WSL 中配置 Git
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

## 其他资源

- [WSL 官方文档](https://learn.microsoft.com/zh-cn/windows/wsl/)
- [WSL 2 安装指南](https://learn.microsoft.com/zh-cn/windows/wsl/install)
- [Windows Terminal](https://aka.ms/terminal)
