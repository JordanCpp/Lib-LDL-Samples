cmake_minimum_required(VERSION 3.25)

add_definitions(-DLDL_STATIC_LIBRARY)

add_subdirectory(dependencies/LDL)

include_directories(dependencies/LDL/include)
link_directories   (${CMAKE_CURRENT_BINARY_DIR}/dependencies/LDL)

add_subdirectory("Tutorials")