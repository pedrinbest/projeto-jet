
cmake_minimum_required(VERSION 3.16)
project(jetski_dashboard C)

set(CMAKE_C_STANDARD 99)

# LVGL
add_subdirectory(lvgl)

# UI exportada pelo SquareLine
add_subdirectory(projeto-jet)

# Executável principal
add_executable(jetski-dashboard
    src/main.c
)

target_include_directories(jetski-dashboard PRIVATE
    lvgl
    lvgl/src
    lvgl/src/drivers/display/fb
    projeto-jet
)

target_link_libraries(jetski-dashboard PRIVATE
    lvgl
    ui
    m
)

