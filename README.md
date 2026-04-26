# Project README

## Overview
This project is a simple C program that calculates and prints the Fibonacci sequence. The code includes a `Main.c` file which serves as the entry point and a `Saved.h` file containing utility functions.

## Features
- Calculates Fibonacci sequence up to a given number.
- Prints the result of the Fibonacci calculation.

## Project Structure
The project structure is organized as follows:

```
Gui_VirtualOS/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── Saved.h         # Header-based C-file containing utility functions
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration for cross-compilation to Windows on Linux
├── Makefile.web        # WebAssembly Build configuration using Emscripten
└── README.md           # This file
└── LICENSE
└── .gitignore
```

## Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools

## Build & Run
The project supports building for different platforms using the provided Makefiles.

### Linux
To build and run on Linux:

```sh
cd Gui_VirtualOS
make -f Makefile.linux all
./build/Main
```

### Windows
To build and run on Windows (Linux cross-compilation):

```sh
cd Gui_VirtualOS
make -f Makefile.wine all
WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
```

### WebAssembly
To build for WebAssembly:

```sh
cd Gui_VirtualOS
make -f Makefile.web all
emrun --no_browser --port 8080 build/index.html
```

This README provides a clear and concise guide to the project, its structure, and how to build and run it on different platforms.