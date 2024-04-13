cmake_minimum_required(VERSION 3.20)
project(Hello_world)

find_package(raylib CONFIG REQUIRED)

set(CMAKE_CXX_STANDARD 17)

add_executable(main src/hello_world.cpp)
target_link_libraries(main PRIVATE raylib)

add_custom_command(TARGET main 
                   POST_BUILD
                   COMMAND ${CMAKE_COMMAND} -E copy $<TARGET_FILE:main> ${PROJECT_SOURCE_DIR})

include_directories(includes)