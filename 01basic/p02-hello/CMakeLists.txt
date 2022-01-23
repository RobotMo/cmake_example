cmake_minimum_required(VERSION 3.5)

project(hello)

set(
    SOURCES
    src/hello.cpp
    src/main.cpp
)

set(
    PROJECT_BINARY_DIR
    build
)

add_executable(hello ${SOURCES})

target_include_directories(
    hello
    PRIVATE
    ${PROJECT_SOURCE_DIR}/include
)

message(${SOURCES})
message(${CMAKE_SOURCE_DIR})
message(${PROJECT_SOURCE_DIR})
message(${CMAKE_BINARY_DIR})
message(${CMAKE_CURRENT_SOURCE_DIR})
message(${CMAKE_CURRENT_BINARY_DIR})
message(${PROJECT_BINARY_DIR})