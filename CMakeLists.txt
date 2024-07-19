# monitor_sys/src/imgui/CMakeLists.txt

cmake_minimum_required(VERSION 3.0)

# ImGui source files
set(IMGUI_SRC
    imgui.cpp
    imgui_draw.cpp
    imgui_demo.cpp
    imgui_widgets.cpp
    imgui_tables.cpp
    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_opengl3.cpp
)

# Create ImGui library
add_library(imgui STATIC ${IMGUI_SRC})

# Include directory for ImGui headers
target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_CURRENT_SOURCE_DIR}/backends)
