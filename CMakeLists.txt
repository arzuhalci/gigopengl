cmake_minimum_required(VERSION 3.0.0)
project(hello_window VERSION 1.0.0)

find_package(OpenGL REQUIRED)

add_subdirectory(dependencies/glfw-3.4)

add_executable(hello_window 
               src/config.h
               src/config.cpp 
               src/main.cpp 
               src/glad.c
               src/triangle_mesh.h
               src/triangle_mesh.cpp
               src/material.cpp)

target_include_directories(hello_window PRIVATE dependencies)

target_link_libraries(hello_window glfw OpenGL::GL)

