add_executable(main_tests
	AllTests.c
	LedDriverTest.c
	LedDriverTestRunner.c
	mocks/RuntimeErrorStub.c
)

target_link_libraries(main_tests
	LedDriver
	Unity
	RuntimeError
)

target_include_directories(main_tests PUBLIC
	mocks
)