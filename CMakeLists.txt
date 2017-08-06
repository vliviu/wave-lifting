cmake_minimum_required (VERSION 2.8.0 FATAL_ERROR)
project (wavelet-2g CXX)

set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14 -Wall -g")

set(RV_SOURCES 	src/main.cpp
)

include_directories("/usr/local/include/eigen3")
set (RV_LIBS ${EXTRA_LIBS} pthread)

add_executable (wavelet2g ${RV_SOURCES})
target_link_libraries (wavelet2g ${RV_LIBS})
