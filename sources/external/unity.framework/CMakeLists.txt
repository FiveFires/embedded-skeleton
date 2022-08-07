add_library(Unity STATIC
    src/unity.c
    extras/fixture/src/unity_fixture.c
)

target_include_directories(Unity PUBLIC
    src
    extras/fixture/src
)
