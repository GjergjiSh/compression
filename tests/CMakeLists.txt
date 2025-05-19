include(FetchContent)
FetchContent_Declare(
    googletest
    URL https://github.com/google/googletest/archive/refs/tags/v1.13.0.zip
    DOWNLOAD_EXTRACT_TIMESTAMP TRUE
)
FetchContent_MakeAvailable(googletest)

enable_testing()

add_executable(compression_tests
    compression_tests.cpp
)

target_link_libraries(compression_tests PRIVATE compression gtest gtest_main)

include(GoogleTest)
gtest_discover_tests(compression_tests)