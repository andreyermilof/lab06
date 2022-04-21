cmake_minimum_required(VERSION 3.0)

project(formatter)

add_library(${PROJECT_NAME} STATIC formatter_.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES
                        CMAKE_BUILD_TYPE Release)
