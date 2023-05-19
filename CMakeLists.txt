# CMake minimum version
cmake_minimum_required(VERSION 3.25)

# C++ version
set(CMAKE_CXX_STANDARD 23)

# Project name
project(FER)

# Files to compile
add_executable(FER src/main.cpp)

# Add all headers in the include directory
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

# GLFW library
target_link_libraries(${PROJECT_NAME} ${CMAKE_CURRENT_SOURCE_DIR}/libs/GLFW/glfw3.lib)
file(COPY ${CMAKE_CURRENT_SOURCE_DIR}/libs/GLFW/glfw3.dll DESTINATION ${CMAKE_CURRENT_BINARY_DIR})