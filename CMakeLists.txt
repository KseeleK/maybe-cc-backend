cmake_minimum_required(VERSION 2.8)

set(CMAKE_CXX_STANDARD 11)

project(llvmIr)

file(GLOB SOURCE
    ${CMAKE_SOURCE_DIR}/src/*.cc
) 

find_package(LLVM REQUIRED)

link_libraries(LLVM)

include_directories(${CMAKE_SOURCE_DIR}/include)

add_executable(out ${SOURCE})