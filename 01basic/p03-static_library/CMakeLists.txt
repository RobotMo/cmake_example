cmake_minimum_required(VERSION 3.5)

project(hello)

add_library(
    libhello
    STATIC
    src/hello.cpp
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
    libhello
)