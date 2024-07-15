idf_component_register(SRCS "tas5806m.c" 
                            "bt_app_core.c" 
                            "bt_app_av.c" 
                            "main.c"
                            PRIV_REQUIRES esp_driver_i2s bt nvs_flash esp_ringbuf esp_driver_dac driver
                            INCLUDE_DIRS "."                 
                    )

idf_build_set_property(COMPILE_OPTIONS "-Wno-format-nonliteral;-Wno-format-security;-Wformat=0" APPEND)