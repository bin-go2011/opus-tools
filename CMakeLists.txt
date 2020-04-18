cmake_minimum_required(VERSION 3.5)
project(OPUS-TOOLS)

add_definitions(-DWIN_UNICODE -DOPUSTOOLS)

find_package(Ogg CONFIG REQUIRED)

include_directories(${CMAKE_SOURCE_DIR}/include
)
if (WIN32)
include_directories(win32)
endif()

add_subdirectory(src)