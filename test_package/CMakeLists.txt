cmake_minimum_required(VERSION 3.15)
project(PackageTest C)

find_package(rpathlink CONFIG REQUIRED)

add_executable(example src/example.c)
target_link_libraries(example rpathlink::rpathlink)
