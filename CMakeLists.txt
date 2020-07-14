cmake_minimum_required(VERSION 3.10)
project(chaosequations)

set(CMAKE_CXX_STANDARD 14)

find_package(SFML COMPONENTS graphics)
set(SFML_STATIC_LIBRARIES TRUE)

find_package(OpenGL REQUIRED)
#include_directories( ${OPENGL_INCLUDE_DIRS} )

include(CMakeRC.cmake)
cmrc_add_resource_library(fonts roboto.ttf)

add_executable(chaosequations Main.cpp)

target_link_libraries(chaosequations PRIVATE fonts)
target_link_libraries(chaosequations PUBLIC  sfml-graphics)
target_link_libraries(chaosequations PUBLIC  ${OPENGL_LIBRARIES})
