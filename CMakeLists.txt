cmake_minimum_required(VERSION 3.10)

project(Render VERSION 1.0)
#configure_file(RenderConfig.h.in RenderConfig.h)

add_executable(Render Render.cpp)
add_subdirectory(libs)
set(SOURCES geometry.h)

target_include_directories(Render PUBLIC "${PROJECT_BINARY_DIR}")
target_link_libraries(Render PUBLIC tgaimage model)

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
target_include_directories(Render PUBLIC
                          "${PROJECT_BINARY_DIR}"
                          "${PROJECT_SOURCE_DIR}/libs"
                          )
