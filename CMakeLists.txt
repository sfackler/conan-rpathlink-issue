cmake_minimum_required(VERSION 3.15)
project(rpathlink C)

find_package(ZLIB CONFIG REQUIRED)

add_library(rpathlink src/rpathlink.c)
target_include_directories(rpathlink PUBLIC include)
target_link_libraries(rpathlink ZLIB::ZLIB)

set_target_properties(rpathlink PROPERTIES PUBLIC_HEADER "include/rpathlink.h")
install(TARGETS rpathlink)
