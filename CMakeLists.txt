cmake_minimum_required(VERSION 3.10)

# set the project name
project(Render VERSION 1.0)
#configure_file(RenderConfig.h.in RenderConfig.h)

# add the executable
add_executable(Render Render.cpp)

target_include_directories(Render PUBLIC "${PROJECT_BINARY_DIR}")
