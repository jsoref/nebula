# Copyright (c) 2020 vesoft inc. All rights reserved.
#
# This source code is licensed under Apache 2.0 License.

nebula_add_test(
    NAME
        http_client_test
    SOURCES
        HttpClientTest.cpp
    OBJECTS
        $<TARGET_OBJECTS:http_client_obj>
        $<TARGET_OBJECTS:ws_obj>
        $<TARGET_OBJECTS:ws_common_obj>
        $<TARGET_OBJECTS:process_obj>
        $<TARGET_OBJECTS:fs_obj>
        $<TARGET_OBJECTS:stats_obj>
        $<TARGET_OBJECTS:time_obj>
        $<TARGET_OBJECTS:base_obj>
        $<TARGET_OBJECTS:version_obj>
    LIBRARIES
        ${PROXYGEN_LIBRARIES}
        gtest
        gtest_main
)
