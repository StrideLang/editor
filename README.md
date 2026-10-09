# Stride Editor (Legacy IDE)

> [!WARNING]
> **Deprecation Notice**: This standalone Qt-based editor (`StrideIDE`) is being retired and is superseded by the official **[VS Code Stride Extension](https://github.com/StrideLang/vscode-stride-lang)**. Active development for language support, syntax highlighting, and editor tooling takes place in the VS Code extension repository.

---

## Overview

`editor` contains the legacy standalone desktop IDE (`StrideIDE`) for the [Stride](https://github.com/StrideLang/Stride) programming language.

It was developed as a dedicated environment for writing, navigating, and building Stride programs and projects.

### Features
* **Code Editor**: Custom syntax highlighting, line numbering, error markers, and search/replace.
* **Code Model & Autocomplete**: Interactive code modeling and context-aware completion menus.
* **Project & Strideroot Management**: Dialogs for configuring platform targets, hardware frameworks (e.g. XMOS), and strideroot libraries.
* **QML & Web Views**: Integrated QML and Qt WebEngine views for visual components.

---

## Alternative: Modern Editor Support

We recommend using Visual Studio Code with the official Stride extension:

* **Repository**: [StrideLang/vscode-stride-lang](https://github.com/StrideLang/vscode-stride-lang)

---

## Building from Source (Legacy)

### Prerequisites

* **CMake** 3.13 or newer
* **C++17** compatible compiler
* **Qt 6** (6.5+ recommended) with modules:
  * `Core`, `Widgets`, `WebEngineCore`, `WebEngineWidgets`, `Qml`
* Stride core libraries (`StrideParser`, `StrideCodegen`)

### Build

Within the central [Stride](https://github.com/StrideLang/Stride) build workspace, or configured standalone against Stride dependencies:

```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --config Release --target StrideIDE
```

---

## License

Stride Editor is licensed under the terms of the 3-clause BSD License.
