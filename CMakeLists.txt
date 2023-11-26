cmake_minimum_required(VERSION 3.26)
project(Wx)

set(CMAKE_CXX_STANDARD 11)

file(GLOB SRC
        ./src/*.h
        ./src/*.cpp
)

add_executable(Wx ${SRC})

find_package(wxWidgets REQUIRED net core base)
include(${wxWidgets_USE_FILE})

target_link_libraries(Wx ${wxWidgets_LIBRARIES})
