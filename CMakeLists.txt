cmake_minimum_required(VERSION 3.31)
project(testgl)

set(CMAKE_CXX_STANDARD 20)

find_package(glfw3 REQUIRED)
find_package(GLEW REQUIRED)
find_package(glm REQUIRED)

find_package(OpenGL REQUIRED)

add_executable(testgl main.cpp.old
        main.cpp
)

target_link_libraries( testgl
        OpenGL::GL
        GLEW::GLEW
        glfw
)
