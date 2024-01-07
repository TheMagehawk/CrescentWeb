---
title: "Contribute"
---

<h1 style="margin-top: -40px; text-align: center;">Setting up Crescent</h1>

{{< toc >}}

## Requirements

- **Git**, **CMake 3.15+** and **Python 3.3+**
- **C/C++ Compiler** (GCC, Clang, Visual C++, ...) and **Generator** (Make, Ninja, Visual Studio, ...)
- **Cross compile Android**: **Android NDK**
- **Cross compile Emscripten/Web**: **Emscripten SDK (Emsdk)**

<ins>Note:</ins> Make sure these tools are available globally/from the PATH. On Windows you might want to tweak your environment variables.

<ins>**Clone the repository and initialize submodules:**</ins>

```
git clone --recursive https://github.com/TheMagehawk/Crescent.git
```

Alternatively:
```
git clone https://github.com/TheMagehawk/Crescent.git
git submodule update --init --recursive --depth=1
```

<ins>**To update to the latest commit**</ins> ✅

```
git pull --recurse-submodules
```

## 🛠️ Build

### 🧰 IDE

- This Project has integrated support on most modern IDEs thanks to CMake and CMake Presets
- Configure the CMake Project (and delete and regenerate Cache if needed or error)
- Run one of the available CMake Presets/Configurations

### 🖨️ CLI

#### 🐧 Linux:
```
chmod +x build.sh && ./build.sh [FLAGS]
```

#### 🖼️ Windows:
```
./build.bat [FLAGS]
```

#### 🍎 MacOS:
```
chmod +x build.sh && ./build.sh [FLAGS]
```

#### 🤖 Android (Experimental right now):
- Cross Compile on **Windows:**
```
./build.bat --android [NDK_PATH]
```
- Cross Compile on **Linux/MacOS:**
```
./build.sh --android [NDK_PATH]
```

#### 🍏 iOS:
- Maybe someday...

#### 🌐 Emscripten/Web:
- Cross Compile on **Windows:**
```
./build.bat --emscripten
```
- Cross Compile on **Linux/MacOS:**
```
./build.sh --emscripten
```

### 🚩 Configuration/Build Flags
To print out all available Build Script flags:
- **Windows:**
```
./build.bat --help
```
- **Linux/MacOS:**
```
./build.sh --help
```

## 🔬🩺 Troubleshooting

In most cases deleting the cache and reconfiguring the CMake Project fixes any build errors:
- **Windows:**
```
./build.bat --clean && ./build.bat [FLAGS]
```
- **Linux/MacOS:**
```
./build.sh --clean && ./build.sh [FLAGS]
```

If you encounter any other unresolved errors, don't hesitate to open an Issue and provide the corresponding error logs and setup details. We will try to fix it as soon as possible :)
