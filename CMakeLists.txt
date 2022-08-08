


cmake_minimum_required (VERSION 3.16.3)
project (MY_IM_GUI)
find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_subdirectory(dear_imgui)
add_subdirectory(imgui_backend)

add_executable(main main.cpp)
target_link_libraries(main PRIVATE imgui ${CMAKE_DL_LIBS} backend_imgui dl glfw OpenGL::GL)

