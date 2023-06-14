# BuildSystem_tutorial

Make is a buildsystem that operates on Makefile 

CMake makes Makefile's. it can produces makefiles for various platforms

Make

structure of a Makefile

target:
    command_to_execute

CMake

Cmake relies on CMakeLists.txt
`Cmake -S [] -B []`
-S: to source of CMakeLists.txt
-B: src to where build, default is current

This will generate many files, important one for us is: Makefile
the Makefile wont build anything for us right now 

Working with CMakeLists.txt
```
cmake_minimum_require(VERSION 3.13.4)
project(anything)
add_executable(${PROJECT_NAME} src.cpp)

```

those three lines are required
in add_executable you need to provide the file that needs to be compiled and the output executable will be of name that is provided in the project()