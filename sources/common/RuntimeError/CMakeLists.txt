add_library(RuntimeError STATIC
	RuntimeError.c)

target_include_directories(RuntimeError PUBLIC
	${CMAKE_CURRENT_LIST_DIR}
)