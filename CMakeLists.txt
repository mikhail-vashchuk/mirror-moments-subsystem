cmake_minimum_required(VERSION 3.20)
project(mirror_moments_subsystem)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(mirror_moments_subsystem
    src/main.cpp
)

target_include_directories(mirror_moments_subsystem PRIVATE include)