cmake_minimum_required(VERSION 3.15)
project(learn-opengl CXX)

add_executable(learn-opengl src/main.cpp)

install(TARGETS learn-opengl DESTINATION "."
        RUNTIME DESTINATION bin
        ARCHIVE DESTINATION lib
        LIBRARY DESTINATION lib
        )

find_package(fmt REQUIRED CONFIG)
find_package(glfw3 REQUIRED CONFIG)
find_package(glad REQUIRED CONFIG)

target_link_libraries(learn-opengl
    PRIVATE
    fmt::fmt
    glfw
    glad::glad
)
