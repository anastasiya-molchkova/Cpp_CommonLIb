cmake_minimum_required(VERSION 3.1.0)

set(PROJECT_CPP_STANDART "cxx_std_17")
set(PROJECT_NAME "CommonLib")
set(LIB_NAME "common")

project(${PROJECT_NAME})

if (CMAKE_BUILD_TYPE STREQUAL "Release")
    set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} /MT")
elseif(CMAKE_BUILD_TYPE STREQUAL "Debug")
    set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} /MTd")
endif()

add_subdirectory(./src)
add_subdirectory(./tests)