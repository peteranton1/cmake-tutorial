# 01 - Installation gcc & CMake

[Back to Index](../README.md)

## Purpose

This folder shows how to install CMake using gcc 

## Install GCC

    $ gcc -h
    Command 'gcc' not found, but can be installed with:
    sudo apt install gcc

    $ sudo apt install gcc
    [sudo] password for myuser: 
    Reading package lists... Done
    Building dependency tree... Done
    Reading state information... Done
    The following additional packages will be installed:
      gcc-13 gcc-13-x86-64-linux-gnu gcc-x86-64-linux-gnu libasan8 libcc1-0
      libgcc-13-dev libhwasan0 libitm1 liblsan0 libquadmath0 libtsan2 libubsan1
    ...
    Setting up gcc (4:13.2.0-7ubuntu1) ...
    Processing triggers for man-db (2.12.0-4build2) ...
    Processing triggers for libc-bin (2.39-0ubuntu8.3) ...

## Install Make 

    $ sudo apt-get install build-essential

## Install CMake

    $ sudo apt-get install cmake

## Install Ninja (optional)

    $ sudo apt install ninja-build

