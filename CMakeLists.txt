cmake_minimum_required(VERSION 3.5.0)
project(hello_window)

find_package(glfw3 3.4 REQUIRED)
find_package(OpenGL REQUIRED)


add_executable(hello_window 
    src/config.h 
    src/main.cpp
    src/glad.c)

target_include_directories(hello_window PRIVATE dependencies)

target_link_libraries(hello_window glfw OpenGL::GL)