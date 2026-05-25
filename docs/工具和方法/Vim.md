# Vim

## 为什么选择Vim

在我看来 Vim 编辑器有如下的好处：

- **全程键盘操作，减少手离开主键区**  

无需鼠标或触控板，光标移动、选择、编辑等操作全部在键盘主键区完成。这极大降低了手部移动带来的时间损耗，长期下来能显著提升编辑流畅度和专注度。

- **组合式编辑语言，提高操作表达力**  

Vim 的操作像一门语言：`d`（删除）、`i`（插入）、`w`（单词）、`$`（行尾）等可以组合，如 `ci"`（修改引号内内容）、`daw`（删除一个单词）。你不再只是“按快捷键”，而是“说出编辑指令”，逻辑清晰且复用性强。

- **几乎所有开发环境都支持 Vim 模式**  

VSCode、IntelliJ、Sublime、Chrome（Vimium）、终端、远程服务器等主流工具都有 Vim 键位插件或原生支持。一次学习，处处可用，不必在不同 IDE 之间切换心智模型。

- **高效处理结构化代码**  

配合 `.`（重复上次修改）、宏录制（`q`）、多文件操作（`:bn`）、标签跳转（`Ctrl-]`）、全局替换（`:s`）等，Vim 在重构、批量修改、跨文件跳转时非常高效。尤其在服务器上通过 SSH 无界面环境下，Vim 几乎是唯一可靠的快速编辑方案。

## 怎么学习 Vim

不幸的是 Vim 的学习曲线确实相当陡峭，我花了好几个星期才慢慢适应了用 Vim 进行开发的过程。最开始你会觉得非常不适应，但一旦熬过了初始阶段，相信我，你会爱上 Vim。

Vim 的学习资料浩如烟海，但掌握它最好的方式还是将它用在日常的开发过程中，而不是一上来就去学各种花里胡哨的高级 Vim 技巧。个人推荐的学习路线如下：

- 先阅读[这篇 tutorial](https://missing.csail.mit.edu/2020/editors/)，掌握基本的 Vim 概念和使用方式，不想看英文的可以阅读[这篇教程](https://wsdjeg.net/vim-galore-zh-cn/)。
- 用 Vim 自带的 `vimtutor` 进行练习，安装完 Vim 之后直接在命令行里输入 `vimtutor` 即可进入练习程序。
- 最后就是强迫自己使用 Vim 进行开发，IDE 里可以安装 Vim 插件。
- 等你完全适应 Vim 之后新的世界便向你敞开了大门，你可以按需配置自己的 Vim（修改 `.vimrc` 文件），网上有数不胜数的资源可以借鉴。
- 如果你想对配置 Vim 有更加深入的了解，[_Learn Vim Script the Hard Way_](https://learnvimscriptthehardway.stevelosh.com/) 是一个很好的资源。

## 键位映射

用 Vim 编辑代码的时候会频繁用到 ESC 和 CTRL 键, 但是这两个键都离 home row 很远, 可以把 CapsLock 键映射到 Esc 或者 Ctrl 键，让手更舒服一些。

Windows 系统可以使用 [Powertoys](https://learn.microsoft.com/en-us/windows/powertoys/) 或者 [AutoHotkey](https://www.autohotkey.com/) 重映射键位。    
MacOS 系统提供了重映射键位的[设置](https://vim.fandom.com/wiki/Map_caps_lock_to_escape_in_macOS)，另外也可以使用 [Karabiner-Elements](https://karabiner-elements.pqrs.org/) 重映射。  
Linux 系统可以使用 [xremap](https://github.com/xremap/xremap) 进行映射，对于 wayland 和 x.org 都可以使用，并且支持分别映射点按和按住。

但更佳的做法是同时将 CapsLock 映射为 Ctrl 和 Esc，点按为 Esc，按住为 Ctrl。这是不同系统下的实现方法：

- [Windows](https://gist.github.com/sedm0784/4443120)  
- [MacOS](https://ke-complex-modifications.pqrs.org/#caps_lock_tapped_escape_held_left_control)  
- [Linux](https://www.jianshu.com/p/6fdc0e0fb266)

## 其他资源

- [vim官方仓库](https://github.com/vim/vim)
- [在浏览器中使用vim](https://github.com/philc/vimium)