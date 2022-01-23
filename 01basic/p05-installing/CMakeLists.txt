cmake_minimum_required(VERSION 3.5)

project(hello)

if( CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT )
  message(STATUS "Setting default CMAKE_INSTALL_PREFIX path to ${PROJECT_SOURCE_DIR}/install")
  set(CMAKE_INSTALL_PREFIX "${PROJECT_SOURCE_DIR}/install" CACHE STRING "The path to use for make install" FORCE)
endif()

add_library(
    libhello_inst
    SHARED
    src/hello.cpp
)

target_include_directories(
    libhello_inst
    PUBLIC
    ${PROJECT_SOURCE_DIR}/include
)

add_executable(
    hello_inst
    src/main.cpp
)

target_link_libraries(
    hello_inst
    PRIVATE
    libhello_inst
)

install(
    TARGETS hello_inst
    DESTINATION bin
)

install(
    TARGETS libhello_inst
    LIBRARY DESTINATION lib
)

install(
    DIRECTORY ${PROJECT_SOURCE_DIR}/include/
    DESTINATION include
)

# install(
#     FILES cmake-example.conf
#     DESTINATION etc
# )