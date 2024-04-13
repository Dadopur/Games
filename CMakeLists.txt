cmake_minimum_required(VERSION 3.20)
project(Hello_world)

find_package(raylib CONFIG REQUIRED)

set(CMAKE_CXX_STANDARD 17)

add_executable(main hello_world.cpp)
target_link_libraries(main PRIVATE raylib)

