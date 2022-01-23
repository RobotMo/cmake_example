project(sub2)

add_library(
    lib${PROJECT_NAME}
    INTERFACE
)
add_library(
    sub::lib2
    ALIAS
    lib${PROJECT_NAME}
)

target_include_directories(
    lib${PROJECT_NAME}
    INTERFACE
    ${PROJECT_SOURCE_DIR}/include
)