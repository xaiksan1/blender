# Project Overview

This is the source code for Blender, the free and open source 3D creation suite. It is a large and complex C/C++ project with extensive Python integration for scripting, addons, and tooling. The build system is based on CMake and is highly customizable.

The codebase is organized into several main directories:
- `source`: The core source code of Blender.
- `intern`: Internal libraries and dependencies.
- `extern`: External libraries and dependencies.
- `scripts`: Python scripts for various purposes, including addons and modules.
- `tests`: Unit and regression tests.

# Building and Running

Building Blender is a complex process that depends on your operating system and desired configuration. The primary build system is CMake. For detailed instructions, refer to the [official build documentation](https://developer.blender.org/docs/handbook/building_blender/).

A typical build process on Linux would look something like this:

```bash
# 1. Clone the repository and submodules
git clone https://git.blender.org/blender.git
cd blender
make update

# 2. Create a build directory
mkdir build
cd build

# 3. Configure the build with CMake
cmake ..

# 4. Build Blender
make
```

**TODO:** The exact CMake command may require additional flags to configure the build to your liking. Refer to the `CMakeLists.txt` file for a full list of build options.

# Development Conventions

*   **Code Style:** The project uses specific coding styles for C/C++ and Python. For Python, `autopep8` and `black` are used for formatting, with a line length of 120 characters. Refer to the `pyproject.toml` file for detailed configuration.
*   **Testing:** The project uses GTest for C/C++ unit tests and has a suite of Python-based tests. The `CMakeLists.txt` file contains options for enabling and configuring different test suites.
*   **Dependencies:** Dependencies are managed through a combination of the `extern` directory and system libraries. The `CMakeLists.txt` file handles the detection and linking of dependencies.
