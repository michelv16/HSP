cmake_minimum_required(VERSION 3.8)

set(This hspTests)

project(${This} C CXX)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

set(Sources
    exampletest.cpp
    )

add_executable(${This} ${Sources})

target_link_libraries(${This}
	gtest_main
	hsp
)

add_test(
	NAME ${This}
	COMMAND ${This}
)
