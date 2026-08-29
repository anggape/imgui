add_library(
  imgui
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
    backends/imgui_impl_sdl3.cpp
    backends/imgui_impl_sdlrenderer3.cpp
    misc/freetype/imgui_freetype.cpp)
target_include_directories(
  imgui
  PUBLIC
    . backends)
target_link_libraries(
  imgui
  PRIVATE
    SDL3::SDL3
    freetype)
target_compile_definitions(
  imgui
  PUBLIC
    IMGUI_ENABLE_FREETYPE
    IMGUI_DISABLE_OBSOLETE_FUNCTIONS)

add_library(imgui::imgui ALIAS imgui)
