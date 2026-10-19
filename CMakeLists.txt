cmake_minimum_required(VERSION 4.2)
project(glad)

set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")

add_library(glad STATIC
	"src/glad.h"
	"src/glad.c"
	"src/khrplatform.h")
target_include_directories(glad
    PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}"
)
