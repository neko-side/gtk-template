cmake_minimum_required(VERSION 4.0.0)

project(test)

find_package(PkgConfig REQUIRED)

pkg_check_modules(GTK REQUIRED gtk4)

include_directories(${GTK_INCLUDE_DIRS})

link_directories(${GTK_LIBRARY_DIRS})

add_executable(test main.c)

target_link_libraries(test ${GTK_LIBRARIES})