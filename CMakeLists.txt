cmake_minimum_required(VERSION 3.0)

project(raygui C)

# Directory Variables
set(RAYGUI_SRC ${RAYGUI_ROOT}/src)

# raygui
add_library(raygui INTERFACE)
file(GLOB sources ${RAYGUI_SRC}/*.h)
set(RAYGUI_HEADERS ${sources})
install(FILES
    ${RAYGUI_HEADERS} DESTINATION include
)
target_include_directories(raygui INTERFACE ${RAYGUI_SRC})