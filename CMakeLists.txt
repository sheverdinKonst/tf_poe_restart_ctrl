cmake_minimum_required(VERSION 3.26)
project(tf_poe_restart_ctrl C)

set(CMAKE_C_STANDARD 11)

add_executable(tf_poe_restart_ctrl src/main.c
        src/mainParam.h
        src/uds_socket_module.c
        src/uds_socket_module.h
        src/parsing_command.c
        src/parsing_command.h
)

INSTALL(TARGETS tf_poe_restart_ctrl RUNTIME DESTINATION /usr/bin/)
