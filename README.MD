# Custom urdl version 0.1 (02.06.2022)

Depends on latest OpenSSL and Boost libraries + buildable as a static library on Windows.

### HOW TO (Windows)
#### Pre-requisites
* Latest CMake installed (https://cmake.org/download/) + PATH added
* Conan package manager installed (https://conan.io/downloads.html) + PATH added
### Build
* Open Developer Command Prompt for VS 2019
* > conan profile new default --detect --force
* > conan install . --build=missing
* > cd build
* > cmake ..
* > msbuild urdl.sln /p:Configuration=Release
