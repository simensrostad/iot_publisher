#
# Copyright (c) 2020 Nordic Semiconductor
#
# SPDX-License-Identifier: LicenseRef-BSD-5-Clause-Nordic
#

cmake_minimum_required(VERSION 3.8.2)

include(../nrf/cmake/boilerplate.cmake NO_POLICY_SCOPE)

include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(iot_publisher)

# NORDIC SDK APP START
target_sources(app PRIVATE src/main.c)
# NORDIC SDK APP END

zephyr_include_directories(src)

add_subdirectory(src/coap_backend)
add_subdirectory(src/mqtt_backend)
