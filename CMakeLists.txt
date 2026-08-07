add_library(ui STATIC
    ui.c
    ui_helpers.c

    screens/ui_Loading.c
    screens/ui_Tela_Principal.c

    components/ui_comp_hook.c

    images/ui_img_fundo_png.c
    images/ui_img_logo_sea_doo_png.c
    images/ui_img_2038326595.c
    images/ui_img_slider_battery2_png.c
    images/ui_img_gas_png.c
    images/ui_img_rpm_png.c

    fonts/ui_font_Medium.c
    fonts/ui_font_Number.c
)

target_include_directories(ui PUBLIC
    .
    ${CMAKE_SOURCE_DIR}
    ${CMAKE_SOURCE_DIR}/lvgl
)


