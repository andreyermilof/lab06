cmake_minimum_required(VERSION 3.0)

project(solver)

add_library(${PROJECT_NAME} STATIC solver_.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES
                        CMAKE_BUILD_TYPE Release)
