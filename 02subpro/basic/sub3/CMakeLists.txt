project(sub3)

add_executable(${PROJECT_NAME}_exe main.cpp)

target_link_libraries(
    ${PROJECT_NAME}_exe
    sub::lib1
    sub::lib2
)