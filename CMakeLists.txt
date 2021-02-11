cmake_minimum_required(VERSION 3.19.4)

project(hello)

add_executable(Start main main.cpp)

install (TARGETS Start DESTINATION bin)
