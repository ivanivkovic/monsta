# Where to store executable binary
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Minimum version of cmake, for future versions
cmake_minimum_required(VERSION 3.19.4)

# Name this project
project(hello)

# Include include directories
include_directories(
	${PROJECT_SOURCE_DIR}/include
	${PROJECT_SOURCE_DIR}/src
)

# Enables .cpp files to add headers in the include folder.
file(GLOB all_SRCS
	"${PROJECT_SOURCE_DIR}/include/*.h"
	"${PROJECT_SOURCE_DIR}/include/*.hpp"
	"${PROJECT_SOURCE_DIR}/src/*.c"
	"${PROJECT_SOURCE_DIR}/src/*.cpp"
)

add_executable(Start ${all_SRCS})
