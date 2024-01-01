cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(picow_blink_project C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Initialize the Raspberry Pi Pico SDK
pico_sdk_init()

# Create the executable
add_executable(picow_blink
    picow_blink.c
)

# Add pico_stdlib library which aggregates commonly used features
target_link_libraries(picow_blink pico_stdlib)

# Add libraries for Pico W WiFi functionality
target_link_libraries(picow_blink pico_cyw43_arch_none)

# Pass WiFi credentials to the program using compile definitions
target_compile_definitions(picow_blink PRIVATE
    WIFI_SSID="Babbayaga"
    WIFI_PASSWORD="9254776877"
)

# Create map/bin/hex/uf2 file in addition to ELF.
pico_add_extra_outputs(picow_blink)
