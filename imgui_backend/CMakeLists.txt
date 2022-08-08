


add_library(backend_imgui imgui_impl_glfw.cpp imgui_impl_opengl3.cpp)
target_link_libraries(backend_imgui PRIVATE imgui)
target_include_directories(backend_imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
