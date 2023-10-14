cmake_minimum_required(VERSION 3.10)
project(opengl-tut)
add_executable("${PROJECT_NAME}" src/Application.cpp)

find_package(OpenGL REQUIRED)

if (OPENGL_FOUND)
    message("opengl found")
    message("include dir: ${OPENGL_INCLUDE_DIR}")
    message("link libraries: ${OPENGL_gl_LIBRARY}")
else (OPENGL_FOUND)
    message("opengl not found")
endif()

target_link_libraries("${PROJECT_NAME}" PRIVATE ${OPENGL_gl_LIBRARY} glfw)
