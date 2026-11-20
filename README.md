# Alder

Alder is a cross-platform C++20 game engine built from scratch, with Windows x64 as its first development and verification target. The project follows Jason Gregory's fourth edition of *Game Engine Architecture* and draws on Hazel's development history. The goal is to build a 3D room in a standalone editor, then load and play it in either the editor or a standalone sample. The companion GameEngineArchitecture repository contains the development roadmaps.

## Build on Windows

Use CMake 4.2 or later and Visual Studio 2026 with the **Desktop development with C++** workload. Open PowerShell in `Alder/`, the directory containing `CMakeLists.txt`.

### Configure

```powershell
cmake -S . -B build -G "Visual Studio 18 2026" -A x64
```

`-S .` selects the current directory as the source directory. `-B build` places generated project files and binaries in the Git-ignored `build/` directory. Configure once to build both Debug and Release.

### Build and run Debug

```powershell
cmake --build build --config Debug
./build/Debug/Alder.exe
```

### Build and run Release

```powershell
cmake --build build --config Release
./build/Release/Alder.exe
```

Both configurations print `Hello, Alder!`. To rebuild after editing the source, run the corresponding `cmake --build` command again.
