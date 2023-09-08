cmake_minimum_required(VERSION 3.27)

project(windows)

add_definitions(-DGLEW_STATIC)

find_library(GLFW NAMES glfw3 HINTS "${CMAKE_SOURCE_DIR}")
find_library(GLEWS NAMES glew32s HINTS "${CMAKE_SOURCE_DIR}")

add_executable(windows main.cpp)

target_link_libraries(windows ${GLFW})
target_link_libraries(windows ${GLEWS})
target_link_libraries(windows opengl32)
