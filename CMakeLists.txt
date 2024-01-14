cmake_minimum_required(VERSION 3.28.1 FATAL_ERROR)
set(PRJ_NAME BattleCity)


project(${PRJ_NAME})

add_executable(${PRJ_NAME} src/main.cpp)
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PRJ_NAME} glfw)