# 03 - Program with Library

[Back to Index](../README.md)

## Purpose

This folder shows A simple example CMake using a Hello World source file. 

## Source files

This example contains the following source files

    random.c  
    random.h  
    random_main.c

## Compile and Run

    $ gcc -o random_main \
        random_main.c random.c -lm

    $ ls
    random.c  
    random.h  
    random_main  
    random_main.c

    $ ./random_main
    0.767554
    1.104780
    1.069596
    1.084488
    0.245279
    0.580639
    0.292428
    1.135251
    0.902894
    0.226394

## Alternative GCC Commands

You can also compile each c file to an object file, 
then link all objects into an executable.

    gcc -c random_main.c
    gcc -c random.c
    gcc -o random_main \
        random_main.o \
        random.o 
        -lm




