cmake_minimum_required(VERSION 3.25)

if (MSVC)
    add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

set(LDL_STATIC_LIBRARY true)
add_definitions(-DLDL_STATIC_LIBRARY)

set(LDL_RENDER_OPENGL3 true)

add_subdirectory(dependencies/LDL/source)
include_directories(dependencies/LDL/include)
link_directories(${CMAKE_CURRENT_BINARY_DIR}/dependencies/LDL)

include_directories(dependencies/glm)

add_subdirectory("JoeyDeVries")