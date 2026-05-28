# GNU Make

## Why use GNU Make

When you start writing C/C++ projects, you may encounter these situations:

- A project has multiple source files, and every compile requires a long command
- Modifying one file forces recompilation of everything, wasting time
- Complex project structures with many compile options are error-prone to manage manually

GNU Make is a build automation tool that automatically executes compilation and linking by reading Makefile. Almost all C/C++ open-source projects use Make (or Make-based build systems) to manage the build process.

**Automated compilation, goodbye to repetitive work**

After defining build rules in a Makefile, simply type `make` to compile the entire project automatically.

**Incremental compilation, only recompile modified files**

Make detects file modification times and only recompiles changed source files, significantly improving build efficiency.

**Cross-platform standard**

Make is part of the POSIX standard, available on Linux, macOS, and Windows (via MSYS2/MinGW).

## Installing GNU Make

**Windows**

```powershell
scoop install make
```

> Note: On Windows, the MSYS2 version of Make is recommended for better compatibility with Unix toolchains.

**macOS**

Make comes with macOS (via Xcode Command Line Tools):

```bash
xcode-select --install
```

**Linux**

```bash
sudo apt install build-essential
```

`build-essential` includes gcc, g++, make, and other basic development tools.

## Basic usage

**Simplest Makefile**

Suppose you have a C project:

```
main.c
utils.c
utils.h
```

Create a `Makefile`:

```makefile
CC = gcc
CFLAGS = -Wall -g

all: main

main: main.c utils.h
	$(CC) $(CFLAGS) -o main main.c utils.c

clean:
	rm -f main
```

Usage:

```bash
make          # Build the project
make clean    # Clean build artifacts
```

**Core concepts of Makefile**

```makefile
target: dependencies
	command
```

- **target**: The file to generate
- **dependencies**: Required files
- **command**: Command to generate the target (must start with Tab)

**Variables**

```makefile
CC = gcc
CFLAGS = -Wall -g -O2
LDFLAGS = -lm
```

**Automatic variables**

```makefile
$@    # Current target filename
$<    # First dependency filename
$^    # All dependency filenames
```

## Real-world example

A more complete Makefile example:

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

## Other resources

- [GNU Make Official Manual](https://www.gnu.org/software/make/manual/)
- [Makefile Tutorial](https://makefiletutorial.com/)
- [Managing Projects with GNU Make](https://www.oreilly.com/library/view/managing-projects-with/9780596800024/) — classic book
