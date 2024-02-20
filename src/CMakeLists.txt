cmake_minimum_required(VERSION 3.22)

# Includes the Pico SDK
include(pico_sdk_import.cmake)

# Replace 'onboard_led_blink' with actual project name
project(picow_blink_project)

# Initializes the Pico SDK
pico_sdk_init()

add_executable(picow_blink
        picow_blink.c
        )

target_link_libraries(picow_blink
        pico_stdlib              # for core functionality
        pico_cyw43_arch_none     # we need Wifi to access the GPIO, but we don't need anything else
        )

# create map/bin/hex file etc.
pico_add_extra_outputs(picow_blink)

# add url via pico_set_program_url
# example_auto_set_url(picow_blink)
