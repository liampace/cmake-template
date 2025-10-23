# Directory Structure
```
cmake/
└── modules/
    └── **.cmake
examples/
└── <EXAMPLE_NAME>/
    ├── **.c
    └── **.cpp
docs/
├── Doxyfile.in
├── DoxygenLayout.xml
└── **.md
include/
└── <PROJECT_NAME>/
    ├── **.h
    └── **.hpp
lib/
└── **/CMakeLists.txt
src/
├── include/
│   └── <PROJECT_NAME>/
│       ├── **.h
│       └── **.hpp
├── <SYSTEM_NAME>/
│   ├── **.c
│   └── **.cpp
└── <PROJECT_NAME>/
    ├── **.c
    └── **.cpp
test/
└── <PROJECT_NAME>/
    ├── **.c
    └── **.cpp
```
---
## CMake Module Files
### Location: `./cmake/modules/`
| File Extension | File Type    |
| -------------- | ------------ |
| `.cmake`       | CMake Module |

---
## Example Files
### Location: `./examples/<EXAMPLE_NAME>/`
| File Extension | Language |
|----------------| -------- |
| `.c`           | C        |
| `.cpp`         | C++      |

NOTE: `<EXAMPLE_NAME>` is an arbitrary name for the example

NOTE: Example files should contain a `main` function

---
## Documentation Files
### Location: `./docs/`
| File              | Purpose                      |
| ----------------- | -----------------------------|
| Doxyfile.in       | Settings for Doxygen         |
| DoxygenLayout.xml | Layout for generated website |
| \*\*.md           | Misc. documentation files    |

---
## Header/Template Files
### Location (Public Headers):  `./include/<PROJECT_NAME>/`
### Location (Private Headers): `./src/include/<PROJECT_NAME>/`
| File Extension | Language |
| -------------- | -------- |
| `.h`           | C        |
| `.hpp`         | C++      |

NOTE: `<PROJECT_NAME>` must match the project name defined in `CMakeLists.txt`

---
## Dependency Files
### Location (Specific Dependency): `./lib/<DEPENDENCY_NAME>/CMakeLists.txt`

NOTE: `<DEPENDENCY_NAME>` must match the project name defined in its `CMakeLists.txt`

---
## Source/Implementation Files
### Location (Platform Dependant): `./src/<SYSTEM_NAME>/`
### Location (Cross Platform): `./src/<PROJECT_NAME>/`
| File Extension | Language |
|----------------| -------- |
| `.c`           | C        |
| `.cpp`         | C++      |

NOTE: `<SYSTEM_NAME>` must match one of the known values for [`CMAKE_SYSTEM_NAME`](https://cmake.org/cmake/help/latest/variable/CMAKE_SYSTEM_NAME.html)

NOTE: `<PROJECT_NAME>` must match the project name defined in `CMakeLists.txt`

---
## Test Files
### Location: `./test/<PROJECT_NAME>/`
| File Extension | Language |
|----------------| -------- |
| `.c`           | C        |
| `.cpp`         | C++      |

NOTE: `<PROJECT_NAME>` must match the project name defined in `CMakeLists.txt`