cmake_minimum_required(VERSION 3.14)
project(BasicSPHSolverNormal)

set(TARGET BasicSPHSolverNormal)

set(SRC ./src)
file(GLOB SOURCEFILES ${SRC}/*.cpp ${SRC}/*.h ${SRC}/*.hpp)

aux_source_directory(. SRC_LIST)
add_executable(${PROJECT_NAME} ${SOURCEFILES})

