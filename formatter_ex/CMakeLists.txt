cmake_minimum_required(VERSION 3.0)

project(formatter_ex)

add_library(${PROJECT_NAME} STATIC formatter_ex_.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES
                        CMAKE_BUILD_TYPE Release)

target_include_directories(${PROJECT_NAME} PUBLIC
                            ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib formatter)

target_link_libraries(${PROJECT_NAME} formatter)
