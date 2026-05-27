cmake_minimum_required (VERSION 3.9.0)
project(OpenGLTutorial)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

include_directories(glad/include)

add_subdirectory(glfw-3.4)

add_executable(OpenGLTutorial
        main.cpp
        glad/src/glad.c
        Shader.cpp
        Shader.h
)

target_link_libraries(OpenGLTutorial glfw)