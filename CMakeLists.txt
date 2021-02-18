cmake_minimum_required(VERSION 3.8)

set(This hsp)
set(gtestDIR /home/michel/Development/tools/googletest)

project(${This} C CXX)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

enable_testing()

add_subdirectory(${gtestDIR} ${PROJECT_SOURCE_DIR})

set(Headers
    )

set(Sources
    main.cpp)

add_library(${This} ${Sources} ${Headers})

add_subdirectory(tests)
