cmake_minimum_required(VERSION 3.15)
project(chaosequations)

set(CMAKE_CXX_STANDARD 14)

find_package(SFML COMPONENTS graphics)
set(SFML_STATIC_LIBRARIES TRUE)

find_package(OpenGL REQUIRED)
#include_directories( ${OPENGL_INCLUDE_DIRS} )

include(CMakeRC.cmake)
cmrc_add_resource_library(roboto.ttf ALIAS font NAMESPACE roboto)

add_executable(chaosequations Main.cpp)

target_link_libraries(chaosequations PUBLIC font)
target_link_libraries(chaosequations PUBLIC sfml-graphics)
target_link_libraries(chaosequations PUBLIC ${OPENGL_LIBRARIES})
