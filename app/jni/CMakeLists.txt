if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})
  message(FATAL_ERROR "Prevented in-tree built. Please create a build directory outside of the SDL source code and call cmake from there")
endif() 

cmake_minimum_required(VERSION 2.8.11)
#project(main C)

add_subdirectory(SDL2)
add_subdirectory(src)
