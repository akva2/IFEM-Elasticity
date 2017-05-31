project(Beam)

cmake_minimum_required(VERSION 2.6)

include_directories(${PROJECT_SOURCE_DIR}/..)

set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib)

file(GLOB Beam_SOURCES RELATIVE ${PROJECT_SOURCE_DIR} *.C)
file(GLOB Beam_HEADERS *.h)
add_library(Beam STATIC ${Beam_SOURCES})

set(Beam_SOURCES ${Beam_SOURCES} PARENT_SCOPE) # Requires for static analysis
