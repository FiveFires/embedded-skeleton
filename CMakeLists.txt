project("LedDriver" C)
cmake_minimum_required(VERSION 3.0)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
set(TARGET_GROUP test CACHE STRING "Group to build")

add_subdirectory(sources/drivers)
add_subdirectory(sources/common)

if(TARGET_GROUP STREQUAL production)
    add_subdirectory(sources/main)
elseif(TARGET_GROUP STREQUAL test)
    add_subdirectory(sources/external)
    add_subdirectory(sources/tests)
else()
    message(FATAL_ERROR "Given TARGET_GROUP unknown")
endif()
