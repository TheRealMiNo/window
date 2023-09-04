cmake_minimum_required(VERSION 3.27)

project(test)

find_library(GLFW NAMES glfw3 HINTS "${CMAKE_SOURCE_DIR}")

add_executable(test main.cpp)

target_link_libraries(test ${GLFW})