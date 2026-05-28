# GNU Make

## 为什么使用 GNU Make

当你开始编写 C/C++ 项目时，你可能会遇到这样的情况：

- 一个项目有多个源文件，每次编译都要手动输入一长串命令
- 修改了一个文件，重新编译时所有文件都要重新编译，浪费时间
- 项目结构复杂，编译选项多，手动管理容易出错

GNU Make 是一个构建自动化工具，它通过读取 Makefile 文件来自动执行编译、链接等操作。几乎所有 C/C++ 开源项目都使用 Make（或基于 Make 的构建系统）来管理构建过程。

**自动化编译，告别重复劳动**

在 Makefile 中定义好编译规则后，只需输入 `make` 即可自动完成整个项目的编译。

**增量编译，只编译修改过的文件**

Make 会检测文件的修改时间，只重新编译发生变化的源文件，大幅提升编译效率。

**跨平台标准**

Make 是 POSIX 标准的一部分，在 Linux、macOS、Windows（通过 MSYS2/MinGW）上都能使用。

## 安装 GNU Make

**Windows**

```powershell
scoop install make
```

> 注意：Windows 上建议使用 MSYS2 版本的 Make，与 Unix 工具链兼容性更好。

**macOS**

macOS 自带 Make（通过 Xcode Command Line Tools）：

```bash
xcode-select --install
```

**Linux**

```bash
sudo apt install build-essential
```

`build-essential` 包含了 gcc、g++、make 等基础开发工具。

## 基本使用

**最简单的 Makefile**

假设你有一个 C 项目：

```
main.c
utils.c
utils.h
```

创建 `Makefile`：

```makefile
CC = gcc
CFLAGS = -Wall -g

all: main

main: main.c utils.h
	$(CC) $(CFLAGS) -o main main.c utils.c

clean:
	rm -f main
```

使用方式：

```bash
make          # 编译项目
make clean    # 清理编译产物
```

**Makefile 的核心概念**

```makefile
target: dependencies
	command
```

- **target**：要生成的文件
- **dependencies**：依赖的文件
- **command**：生成 target 需要执行的命令（必须以 Tab 开头）

**变量**

```makefile
CC = gcc
CFLAGS = -Wall -g -O2
LDFLAGS = -lm
```

**自动变量**

```makefile
$@    # 当前目标文件名
$<    # 第一个依赖文件名
$^    # 所有依赖文件名
```

## 实际项目示例

一个更完整的 Makefile 示例：

```makefile
CC = gcc
CFLAGS = -Wall -g
LDFLAGS = -lm
SRC = $(wildcard *.c)
OBJ = $(SRC:.c=.o)
TARGET = myprogram

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CC) $(OBJ) -o $(TARGET) $(LDFLAGS)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ) $(TARGET)

.PHONY: all clean
```

## 其他资源

- [GNU Make 官方手册](https://www.gnu.org/software/make/manual/)
- [Makefile 教程](https://makefiletutorial.com/)
- [Managing Projects with GNU Make](https://www.oreilly.com/library/view/managing-projects-with/9780596800024/) — 经典书籍
