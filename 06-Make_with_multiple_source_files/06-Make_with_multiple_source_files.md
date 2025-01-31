# 06-Make_with_multiple_source_files

[Back to Index](../README.md)

## Purpose

Using multiple source files,
here is an example of Make.

## Make file with multiple source files

    # Compiler to use
    CC = gcc
    
    # Compiler flags:
    # -Wall: Enable all warning messages
    # -Wextra: Enable extra warning flags
    # -g: Include debugging information
    CFLAGS = -Wall -Wextra -g
    
    # Target executable name
    TARGET = random_main
    
    # Source files
    SRCS = random_main.c random.c
    
    # Object files (replace .c with .o)
    OBJS = $(SRCS:.c=.o)
    
    # Include Maths library
    LIBS = -lm
    
    # Default rule to build target
    all: $(TARGET)
    
    # Link object files to create the executable
    $(TARGET): $(OBJS)
        $(CC) $(CFLAGS) -o $(TARGET) $(OBJS) $(LIBS)
    
    # Compile source files with object files
    %.o: %.c
        $(CC) -c $< -o $@
    
    # Clean up build files
    clean:
        rm -f $(OBJS) $(TARGET)


## Running make

    $ make

## Running just compile for individual source

    $ make random.o

## Clean all

    $ make clean





