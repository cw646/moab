

cmake_minimum_required(VERSION 3.6)
project(MOAB_Example)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES main.cpp)
add_executable(moab ${SOURCE_FILES})

# MOAB
find_package(MOAB)
if (MOAB_FOUND)
    include_directories(${MOAB_INCLUDE_DIRS})
endif()
