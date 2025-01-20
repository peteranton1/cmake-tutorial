# 05 - Program with make

[Back to Index](../README.md)

## Purpose

This folder building from source with two source files. 

## Source files

This example contains the following source files

    random.c  
    random.h  
    random_main.c

There is also an extra file called Makefile

## Make file for >1 source files

Here are the contents of the Makefile

    # Default rule to build the target
    all: random_main
    
    # Link object files to create the executable
    random_main: random_main.c
        gcc -o random_main \
            random_main.c \
            random.c \
            -lm
    
    # Clean up build files
    clean:
        rm -f random_main

## Make Clean

You can remove intermediate files 
with the following command.

    $ make clean




