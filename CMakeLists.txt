set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 17)

add_library(imgui STATIC "imgui.cpp"
                         "imgui_demo.cpp"
                         "imgui_draw.cpp"
                         "imgui_tables.cpp"
                         "imgui_widgets.cpp"
                         "imgui.h"
                         "imconfig.h"
                         "imgui_internal.h"
                         "imstb_rectpack.h"
                         "imstb_textedit.h"
                         "imstb_truetype.h")

target_include_directories(imgui INTERFACE .)

set_property(TARGET imgui PROPERTY POSITION_INDEPENDENT_CODE ON)
