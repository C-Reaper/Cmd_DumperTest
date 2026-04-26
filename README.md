# Project README

## Overview
This project is a C application that demonstrates the use of custom data structures (vectors), serialization, and deserialization. The application uses a custom library to manage dynamic arrays and provides functionality to dump and load these vectors in a binary format.

## Features
- Dynamic vector management
- Serialization and deserialization of vectors into binary files
- Debugging capabilities via Makefile targets

## Project Structure
```
Cmd_DumperTest/
├── build/              # .exe files produced by Main.c
├── src/                # source code
│   ├── Main.c          # Entry point
│   └── *.h             # header-based C-files, without implementation in *.c
└── Makefile.linux      # Linux Build configuration
└── Makefile.windows    # Windows Build configuration
└── Makefile.wine       # Wine Build configuration
└── Makefile.web        # Emscripten Build configuration
└── README.md           # This file
└── LICENSE
└── .gitignore
```

## Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools

## Build & Run
### Linux
1. Navigate to the project directory:
   ```sh
   cd Cmd_DumperTest/
   ```
2. Build the application:
   ```sh
   make -f Makefile.linux all
   ```
3. Run the application:
   ```sh
   ./build/Main
   ```

### Windows
1. Navigate to the project directory:
   ```sh
   cd Cmd_DumperTest/
   ```
2. Build the application:
   ```sh
   make -f Makefile.windows all
   ```
3. Run the application:
   ```sh
   build\Main.exe
   ```

### Wine
1. Navigate to the project directory:
   ```sh
   cd Cmd_DumperTest/
   ```
2. Build the application:
   ```sh
   make -f Makefile.wine all
   ```
3. Run the application:
   ```sh
   WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
   ```

### WebAssembly
1. Navigate to the project directory:
   ```sh
   cd Cmd_DumperTest/
   ```
2. Build the application:
   ```sh
   make -f Makefile.web all
   ```
3. Run the application using wasmtime:
   ```sh
   wasmtime build/Main.wasm
   ```

### Clean Build
To clean and rebuild the project, use:
```sh
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

Where `(os)` can be `linux`, `windows`, `wine`, or `web` depending on your target platform.