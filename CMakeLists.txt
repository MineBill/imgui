cmake_minimum_required(VERSION 3.24)

project(imgui VERSION 1.89.2)

add_library(imgui
        imgui.cpp
        imgui.h
        imgui_demo.cpp
        imgui_draw.cpp
        imgui_internal.h
        imgui_tables.cpp
        imgui_widgets.cpp
        imstb_rectpack.h
        imstb_textedit.h
        imstb_truetype.h

        misc/cpp/imgui_stdlib.cpp
        misc/cpp/imgui_stdlib.cpp

        backends/imgui_impl_opengl3.h
        backends/imgui_impl_opengl3.cpp
        backends/imgui_impl_opengl3_loader.h
        backends/imgui_impl_glfw.h
        backends/imgui_impl_glfw.cpp)

target_link_libraries(imgui glfw glm::glm)

target_include_directories(imgui SYSTEM PUBLIC .)
