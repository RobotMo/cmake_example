project (sub1)

# Add a library with the above sources
add_library(lib${PROJECT_NAME} src/sublib1.cpp)
add_library(sub::lib1 ALIAS lib${PROJECT_NAME})

target_include_directories( lib${PROJECT_NAME}
    PUBLIC ${PROJECT_SOURCE_DIR}/include
)