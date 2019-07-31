cmake_minimum_required (VERSION 3.7)
project (HelloWindow)

set(SRC_DIR "${PROJECT_SOURCE_DIR}/src")
set(CMAKE_CXX_STANDARD 11)

set(sources "${SRC_DIR}/main.cpp" "${SRC_DIR}/glad.c")

include_directories(include src)

find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)
# find_package(GLEW 2.0 REQUIRED)

#set(LIBRARIES glfw ${OPENGL_LIBRARY} GLEW::GLEW)
set(LIBRARIES glfw ${OPENGL_LIBRARY})

add_executable(HelloWindow ${sources})
target_link_libraries(HelloWindow ${LIBRARIES})