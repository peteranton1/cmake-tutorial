# 04 - Hello World with Make

[Back to Index](../README.md)

## Purpose

This folder shows A simple example 
of compiling a c program
using a Hello World source file.

There is an extra file called Makefile

## Make file for 1 source file

    # Default rule to build the target
    all: hello

    # Link object files to create the executable
    hello: hello.c
        gcc -o hello hello.c

    # Clean up build files
    clean:
        rm -f hello

## Running make

    $ make hello

    $ ls
    04-Hello_World_with_Make.md  
    hello.c  
    Makefile

    $ ./hello
    Hello World




