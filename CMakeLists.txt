cmake_minimum_required(VERSION 3.8)
project(SDL2Test)

find_package(SDL2 REQUIRED)
include_directories(Test ${SDL2_INCLUDE_DIRS})
string(STRIP ${SDL2_INCLUDE_DIRS} SDL2_INCLUDE_DIRS)
string(STRIP ${SDL2_LIBRARIES} SDL2_LIBRARIES)

add_executable(Test main.cpp)
target_link_libraries(Test ${SDL2_LIBRARIES})