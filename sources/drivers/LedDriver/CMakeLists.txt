add_library(LedDriver STATIC
	LedDriver.c)

target_include_directories(LedDriver PUBLIC
	${CMAKE_CURRENT_LIST_DIR}
)

target_link_libraries(LedDriver
    RuntimeError
)