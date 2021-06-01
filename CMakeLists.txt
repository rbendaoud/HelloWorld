cmake_minimum_required(VERSION 3.0.0)
project(HelloWorld VERSION 0.1.0)

SET(GCC__COMPILE_FLAGS "-std=c++2a")

SET(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS}  ${GCC__COMPILE_FLAGS}")

include(CTest)

enable_testing()

file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/*.cpp")

add_executable(HelloWorld ${SOURCES})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
