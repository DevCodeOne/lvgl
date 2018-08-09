cmake_minimum_required(VERSION 3.6.2)
project(lvgl C CXX)
set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

add_compile_options(-Wall -Wextra -Wpedantic -Wno-psabi -g)

file(GLOB SRC_FILES src/*/*.c)
add_library(lvgl ${SRC_FILES})

target_include_directories(lvgl PUBLIC src/lv_core)
target_include_directories(lvgl PUBLIC src/lv_draw)
target_include_directories(lvgl PUBLIC src/lv_hal)
target_include_directories(lvgl PUBLIC src/lv_misc/lv_fonts)
target_include_directories(lvgl PUBLIC src/lv_misc)
target_include_directories(lvgl PUBLIC src/lv_objx)
target_include_directories(lvgl PUBLIC src/lv_themes)
target_include_directories(lvgl PUBLIC src)
