add_library(imgui STATIC "imgui.cpp"
                         "imgui_demo.cpp"
                         "imgui_draw.cpp"
                         "imgui_widgets.cpp"
                         "imgui.h"
                         "imconfig.h"
                         "imgui_internal.h"
                         "imstb_rectpack.h"
                         "imstb_textedit.h"
                         "imstb_truetype.h")

# Equivalent to compile with -fPIC in Linux
# set(CMAKE_POSITION_INDEPENDENT_CODE ON) # For all targets
set_property(TARGET imgui PROPERTY POSITION_INDEPENDENT_CODE ON)

# set(CMAKE_CXX_STANDARD_REQUIRED ON)
# set(CMAKE_CXX_STANDARD 17) # For all targets
target_compile_features(imgui PRIVATE cxx_std_17)

target_include_directories(imgui INTERFACE .)

target_link_libraries(imgui PUBLIC ${OPENGL_LIBRARIES})
