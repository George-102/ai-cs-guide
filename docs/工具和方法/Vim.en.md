# Vim

## Why choose Vim

In my opinion, the Vim editor has the following benefits:

- **Operate entirely through the keyboard, minimizing the need to take your hands off the main key area**

Without the need for a mouse or touchpad, cursor movement, selection, editing, and other operations can all be completed using the main keys on the keyboard. This significantly reduces the time loss caused by hand movement, and over the long term, it can notably enhance editing fluency and focus.

- **Combined editing language, enhancing operational expression**

Vim's operations are like a language: `d` (delete), `i` (insert), `w` (word), `$` (end of line), etc., which can be combined, such as `ci"` (modify the content within quotation marks) and `daw` (delete a word). You are no longer just "pressing shortcut keys", but "speaking editing commands", with clear logic and strong reusability.

- **Almost all development environments support Vim mode**

VSCode, IntelliJ, Sublime, Chrome (Vimium), Terminal, remote servers, and other mainstream tools all have Vim keystroke plugins or native support. Once you learn, you can use it everywhere, without having to switch mental models between different IDEs.

- **Efficiently handle structured code**

With features such as `.` (repeat last change), macro recording (`q`), multi-file operations (`:bn`), tag navigation (`Ctrl-]`), and global substitution (`:s`), Vim is highly efficient in refactoring, batch modification, and cross-file navigation. Especially in a server environment without a graphical interface via SSH, Vim is almost the only reliable and fast editing solution.

## How to learn Vim

Unfortunately, the learning curve of Vim is indeed quite steep. It took me several weeks to gradually adapt to the process of developing with Vim. At first, you may feel very uncomfortable, but once you get through the initial stage, trust me, you will fall in love with Vim.

- There is an abundance of learning materials for Vim, but the best way to master it is to use it in daily development processes, rather than jumping straight to learning various fancy advanced Vim techniques. Here is my recommended learning path:

  - First, read [this tutorial](https://missing.csail.mit.edu/2020/editors/) to grasp basic Vim concepts and usage. If you prefer not to read in English, you can also read [this tutorial](https://wsdjeg.net/vim-galore-zh-cn/).
  - Use the built-in `vimtutor` command in Vim for practice. After installing Vim, simply enter `vimtutor` in the command line to access the practice program.
  - Lastly, force yourself to use Vim for development. You can install Vim plugins in your IDE.
  - Once you fully adapt to Vim, a new world will open up for you. You can configure your own Vim as needed (by modifying the `.vimrc` file), and there are countless resources available online for reference.
  - If you want to gain a deeper understanding of configuring Vim, [Learn Vim Script the Hard Way](https://learnvimscriptthehardway.stevelosh.com/) is a great resource.

## Key mapping

When editing code with Vim, you frequently use the ESC and CTRL keys, but both of them are far away from the home row. You can map the CapsLock key to the Esc or Ctrl key to make your hands more comfortable.

On Windows systems, you can use [Powertoys](https://learn.microsoft.com/en-us/windows/powertoys/) or [AutoHotkey](https://www.autohotkey.com/) to remap key mappings.     
The macOS system provides a [setting](https://vim.fandom.com/wiki/Map_caps_lock_to_escape_in_macOS) for remapping key mappings, and you can also use [Karabiner-Elements](https://karabiner-elements.pqrs.org/) for remapping.   
Linux systems can utilize [xremap](https://github.com/xremap/xremap) for mapping, which is compatible with both Wayland and X.Org, and supports separate mapping for single-tap and long-press actions.

- But a better approach is to map CapsLock to both Ctrl and Esc simultaneously, where tapping it corresponds to Esc and holding it down corresponds to Ctrl. Here are the implementation methods for different systems:

  - [Windows](https://gist.github.com/sedm0784/4443120)  
  - [MacOS](https://ke-complex-modifications.pqrs.org/#caps_lock_tapped_escape_held_left_control)  
  - [Linux](https://www.jianshu.com/p/6fdc0e0fb266)

## Other resources

- [Vim official repository](https://github.com/vim/vim)
- [Using Vim in the Browser](https://github.com/philc/vimium)