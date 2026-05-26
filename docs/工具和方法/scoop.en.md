# Scoop

## Why use Scoop

Setting up a development environment on Windows has always been a complex and challenging task. The absence of a unified standard has led to significant differences in the installation methods of various development environments, resulting in unnecessary time costs. Scoop, however, can assist you in uniformly installing and managing common development software, eliminating tedious steps such as manual downloads, installations, and configuration of environment variables.

Scoop will automatically configure the downloaded software into the environment variables, eliminating the hassle of manually configuring the development environment for software on Windows.

For example, to install Python and Node.js, you only need to execute:

```powershell
scoop install python
scoop install nodejs
```

You can even use scoop to download many desktop software, such as QQ Music, Bilibili, WeChat, etc

```
scoop install qqmusic
scoop install bilibili
scoop install wechat
```

## Install Scoop

Scoop requires [Windows PowerShell 5.1](https://aka.ms/wmf5download) or [PowerShell](https://aka.ms/powershell) as its runtime environment. If you are using Windows 10 or later versions, Windows PowerShell is built-in to the system. However, the version of Windows PowerShell built-in to Windows 7 is outdated, and you will need to manually install a newer version of PowerShell.

> Installing software in the user directory using Scoop's default method may cause execution errors for some software. Therefore, it is recommended to install it in a custom directory. For official installation instructions, please refer to [Scoop](https://scoop.sh/)

```powershell
# Set PowerShell execution policy
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
# Download and install script
irm get.scoop.sh -outfile 'install.ps1'
# Execute the installation, with the --ScoopDir parameter specifying the Scoop installation path
.\install.ps1 -ScoopDir 'C:\Scoop'
```

## Use Scoop

The official documentation for Scoop is highly user-friendly for beginners. Rather than belaboring the points here, I recommend reading the [official repository documentation](https://github.com/ScoopInstaller/scoop) or visiting the [quick start guide](https://scoop.sh/).