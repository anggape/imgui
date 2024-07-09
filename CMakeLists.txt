cmake_minimum_required(VERSION 3.29)
project(k_imgui LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_library(
  k_imgui OBJECT
  imgui.cpp imgui_demo.cpp imgui_draw.cpp imgui_tables.cpp imgui_widgets.cpp)
target_include_directories(
  k_imgui
  PUBLIC .)
