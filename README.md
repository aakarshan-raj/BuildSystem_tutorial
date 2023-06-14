# BuildSystem_tutorial

Make is a build system that operates on Makefiles.

CMake makes Makefiles. It can produce makefiles for various platforms.

## Make

### Structure of a Makefile

```makefile
target:
    command_to_execute
```

CMake
CMake relies on CMakeLists.txt. To generate makefiles, use the following command:

`cmake -S [source_path] -B [build_path]`

Where:

-S: to source of CMakeLists.txt
-B: src to where build, default is current

This will generate many files, important one for us is: Makefile
the Makefile wont build anything for us right now 

Working with CMakeLists.txt

The following three lines are required in CMakeLists.txt:


```
cmake_minimum_require(VERSION 3.13.4)
project(anything)
add_executable(${PROJECT_NAME} src.cpp)

```

In the add_executable line, you need to provide the file that needs to be compiled. The output executable will have the name provided in the project().



After setting up the CMakeLists.txt file, run CMake and provide the source of the CMakeLists.txt and the build directory. CMake will generate the Makefile for you. Using that Makefile, you can compile and generate binaries for your project.

