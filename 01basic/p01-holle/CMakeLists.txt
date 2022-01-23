cmake_minimum_required(VERSION 3.5)

set (CMAKE_C_COMPILER "D:/Programs/mingw-64/mingw64/bin/gcc.exe")
set (CMAKE_CXX_COMPILER "D:/Programs/mingw-64/mingw64/bin/g++.exe")
# set (CMAKE_MAKE_PROGRAM "D:/Programs/mingw-64/mingw64/bin/make.exe")

project(holle_cmake)

add_executable(holle main.cpp)