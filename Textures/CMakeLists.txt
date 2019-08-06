cmake_minimum_required (VERSION 3.7)
project (Textures)

set(SRC_DIR "${PROJECT_SOURCE_DIR}/src")
set(CMAKE_CXX_STANDARD 11)

include_directories(include src)

find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)
# find_package(GLEW 2.0 REQUIRED)

#set(LIBRARIES glfw ${OPENGL_LIBRARY} GLEW::GLEW)
set(LIBRARIES glfw ${OPENGL_LIBRARY})

add_executable(Textures "${SRC_DIR}/textures.cpp" "${SRC_DIR}/glad.c" "${SRC_DIR}/stb_image.cpp")
target_link_libraries(Textures ${LIBRARIES})

add_executable(TexturesCombined "${SRC_DIR}/textures_combined.cpp" "${SRC_DIR}/glad.c" "${SRC_DIR}/stb_image.cpp")
target_link_libraries(TexturesCombined ${LIBRARIES})