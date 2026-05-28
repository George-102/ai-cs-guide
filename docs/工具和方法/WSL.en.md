# WSL

## Why use WSL

Many CS course labs use Linux, but most students have Windows computers. Although dual-boot or virtual machines are options, both have drawbacks:

- Dual-boot is cumbersome, can't use Windows and Linux simultaneously
- Virtual machines are resource-heavy and slow
- Some software only runs on Linux

WSL (Windows Subsystem for Linux) lets you run Linux directly on Windows without virtual machines or dual-boot. It's lightweight, fast, and integrates seamlessly with the Windows filesystem.

**No virtual machine, native performance**

WSL 2 uses a real Linux kernel, delivering near-native Linux performance without installing a complete virtual machine.

**Seamless Windows integration**

Linux and Windows filesystems can access each other. In WSL, you can access Windows files (like `/mnt/c/Users/`), and in Windows you can access WSL files.

**Excellent development experience**

Tools like VS Code and Docker Desktop have great WSL support, providing a nearly identical Linux development experience.

**Essential for course labs**

Many CS courses (operating systems, networking, databases) have Linux-based labs. WSL is the best solution for Windows users.

## Installing WSL

Run in PowerShell (as Administrator):

```powershell
# Install WSL 2 and default Ubuntu distribution
wsl --install
```

Restart your computer after installation. Ubuntu will be installed automatically. You'll need to set a username and password on first launch.

**Install a specific distribution**

```powershell
# List available distributions
wsl --list --online

# Install a specific distribution
wsl --install -d Ubuntu-22.04
```

**Set WSL 2 as default version**

```powershell
wsl --set-default-version 2
```

## Basic usage

**Starting WSL**

```powershell
# Start default distribution in PowerShell
wsl

# Start a specific distribution
wsl -d Ubuntu-22.04
```

**Installing software in WSL**

Ubuntu in WSL can use `apt` to install software:

```bash
sudo apt update
sudo apt install build-essential    # Install gcc, g++, make
sudo apt install python3 python3-pip
sudo apt install git
```

**Accessing Windows files**

```bash
# Access Windows C drive from WSL
cd /mnt/c/Users/your_username/

# Access Windows Desktop
cd /mnt/c/Users/your_username/Desktop/
```

**Accessing WSL files from Windows**

Enter `\\wsl$\` in File Explorer's address bar to access WSL's filesystem.

## Recommended setup

**Install Windows Terminal**

Install [Windows Terminal](https://aka.ms/terminal) from the Microsoft Store for a better terminal experience with multiple tabs and customizable themes.

**Use WSL in VS Code**

After installing the WSL extension for VS Code, type `code .` in WSL to open the current directory in VS Code. All operations execute in the WSL environment.

**Configure Git**

```bash
# Configure Git in WSL
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## Other resources

- [WSL Official Documentation](https://learn.microsoft.com/en-us/windows/wsl/)
- [WSL 2 Installation Guide](https://learn.microsoft.com/en-us/windows/wsl/install)
- [Windows Terminal](https://aka.ms/terminal)
