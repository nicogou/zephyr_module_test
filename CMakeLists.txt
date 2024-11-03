# SPDX-License-Identifier: Apache-2.0
if(CONFIG_ZEPHYR_MODULE_TEST)
add_library(zephyr_module_test INTERFACE)

#target_include_directories(mymodule INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
zephyr_include_directories(.)

zephyr_library()
zephyr_library_sources(
    zephyr_module_test.c
    )
zephyr_library_link_libraries(zephyr_module_test)
target_link_libraries(zephyr_module_test INTERFACE zephyr_interface)
endif()
