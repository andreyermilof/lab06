cmake_minimum_required(VERSION 3.0)

project(solve_app)

add_executable(${PROJECT_NAME} solve_app_.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES
                        CMAKE_BUILD_TYPE Release)

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib
                                                   ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib solver)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex formatter_ex)

target_link_libraries(${PROJECT_NAME} formatter_ex solver)
