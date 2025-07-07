cmake_minimum_required(VERSION 3.10)
project(OpenGLProject)

set(CMAKE_CXX_STANDARD 17)

# Include GLAD and GLFW
include_directories(include)
add_subdirectory(src)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

add_executable(OpenGLApp main.cpp)

target_link_libraries(OpenGLApp PRIVATE glad glfw OpenGL::GL)
