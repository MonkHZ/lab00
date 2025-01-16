cmake_minimum_required(VERSION 3.27)
project(lab00)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)

add_executable(lab00
        arrayFuncs.cpp
        arrayFuncs.h
        lab00Test.cpp
        tddFuncs.cpp
        tddFuncs.h)
