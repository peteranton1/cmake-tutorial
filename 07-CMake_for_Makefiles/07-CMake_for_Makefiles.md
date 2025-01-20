# 07-CMake_for_Makefiles

[Back to Index](../README.md)

## Purpose

If you need to generate Makefiles, that is where CMake comes in.

## Need for CMake

Makefile complexity

- As a project increases in size, so can its Makefile
- Add in cross-platform options and flags and the complexity increases even more
- The Makefile for the Linux kernel is 2082 lines long!

So now we need to automate the creation of Makefiles
so Make can automate the compiling of the source code.

This is where CMake fits in. It could stand for 
Create Make but actually the "C" in CMake stands for 
"cross-platform".

## CMake

CMake uses a configuration file called CMakeLists.txt.

1. Define your project in CMakeLists.txt
2. Run CMake to create the Makefile
3. Build your project using Make
4. Add code, fix things, etc then jump to step 3.
5. If you add new .c files or alter the dependencies then jump to step 1.

## Out-of-source builds

Traditionally Makefiles are placed in the same directory as the source code.
You go into the source directory and then run Make. 

CMake is different. The Makefile is generated
in a different directory.

The CMakeLists.txt file is in the source directory, but the automatically 
generated build files are separate, so as not to
overwhelm your source directory.


## Example 1 : Hello

Directory structure

- /home/user/repo/src/hello
  - hello.c
  - CMakeLists.txt
  - build/
    - Makefile
    - CMakeCache.txt
    - cmake_install.cmake
    - CMakeFiles/
    - hello

### Run CMake

    $ cd hello
    $ cd build
    $ cmake ..
    $ ls

## Example 2 : Random

Directory structure

- /home/user/repo/src/random
  - random_main.c
  - random.c
  - random.h
  - CMakeLists.txt
  - build/
    - Makefile
    - CMakeCache.txt
    - cmake_install.cmake
    - CMakeFiles/
    - random_main

### Run CMake

    $ cd random
    $ cd build
    $ cmake ..
    $ ls

