cmake_minimum_required(VERSION 3.26)
project(BasicSPHSolverNode)

set(CMAKE_CXX_STANDARD 17)

set(TARGET BasicSPHSolverNode)

# Load Source
add_library(
        ${TARGET}
        SHARED
        Entrance.cpp
        solver.cpp
        solver.h
        SpatialGrid.h
        SpatialGrid.hpp
)

# Link Houdini Toolkit
target_link_libraries(
        ${TARGET}
        PUBLIC
        Houdini
)
target_include_directories(
        ${TARGET}
        PRIVATE
        ${CMAKE_CURRENT_BINARY_DIR}
)
houdini_configure_target(${TARGET})
