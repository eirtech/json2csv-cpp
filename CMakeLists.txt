cmake_minimum_required(VERSION 3.4)
project(JsonToCVS)

add_definitions(-Wall -g -std=c++14)

find_package(PkgConfig REQUIRED)
pkg_check_modules(JSONCPP jsoncpp)
link_libraries(${JSONCPP_LIBRARIES})
add_executable(JsonToCVS jsontocsv.cpp)
target_link_libraries(JsonToCVS ${JSONCPP_LIBRARIES})
