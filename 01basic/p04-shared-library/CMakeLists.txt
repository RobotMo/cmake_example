cmake_minimum_required(VERSION 3.5)

project(hello)

add_library(
    libhello
    SHARED
    src/hello.cpp
)

add_library(
    hello::library
    ALIAS
    libhello
)

target_include_directories(
    libhello
    PUBLIC
    ${PROJECT_SOURCE_DIR}/include
)

add_executable(
    hello
    src/main.cpp
)

target_link_libraries(
    hello
    PRIVATE
    hello::library
)