cmake_minimum_required (VERSION 3.7)
project (HelloWindow)

set(CMAKE_CXX_STANDARD 11)

find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)
# find_package(GLEW 2.0 REQUIRED)

#set(LIBRARIES glfw ${OPENGL_LIBRARY} GLEW::GLEW)
set(LIBRARIES glfw ${OPENGL_LIBRARY})

add_executable(HelloWindow main.cpp)
target_link_libraries(HelloWindow ${LIBRARIES})