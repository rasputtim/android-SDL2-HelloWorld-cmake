if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR})
  message(FATAL_ERROR "Prevented in-tree built. Please create a build directory outside of the SDL source code and call cmake from there")
endif() 

cmake_minimum_required(VERSION 2.8.11)
project(main CXX) 

set(SRC_PATH ${CMAKE_CURRENT_SOURCE_DIR})
message(STATUS "SOURCE_DIR:  ${SRC_PATH}")
set(SOURCE_FILES
${SRC_PATH}/52_hello_mobile.cpp
)
include_directories(${CMAKE_SOURCE_DIR}/SDL2/include)

add_library(main SHARED ${SOURCE_FILES})
target_link_libraries(main SDL2 GLESv1_CM GLESv2 log)
