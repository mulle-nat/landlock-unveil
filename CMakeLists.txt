cmake_minimum_required(VERSION 3.0)
project(llunveil)

add_library(llunveil llunveil/llunveil.c)
target_include_directories(llunveil PUBLIC llunveil)


option(LLUNVILE_BUILD_EXAMPLES "Build examples" ON)
if(LLUNVILE_BUILD_EXAMPLES)
	add_executable(lljail examples/lljail.c)
	target_link_libraries(lljail PRIVATE llunveil)
endif()