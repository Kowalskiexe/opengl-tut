cmake_minimum_required(VERSION 3.10)
project(opengl-tut)
add_executable("${PROJECT_NAME}" src/Application.cpp)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)

target_link_libraries("${PROJECT_NAME}" PRIVATE ${OPENGL_gl_LIBRARY} ${GLEW_LIBRARIES} glfw)
