cmake_minimum_required(VERSION 3.11)

project(interval-tree)

add_library(interval-tree INTERFACE)

target_include_directories(interval-tree INTERFACE
    $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)

install(
    DIRECTORY ${PROJECT_SOURCE_DIR}/include/
    DESTINATION include
)