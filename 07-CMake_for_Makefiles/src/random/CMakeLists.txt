cmake_minimum_required(VERSION 3.10)

project(random_main)

add_executable(random_main random_main.c random.c random.h)

target_link_libraries(random_main PRIVATE m)
