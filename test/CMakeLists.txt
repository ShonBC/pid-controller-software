set(GTEST_SHUFFLE 1)

add_executable(
    cpp-test
    main.cpp
    pid_test.cpp
)

target_include_directories(cpp-test PUBLIC ../vendor/googletest/googletest/include 
                                           ${CMAKE_SOURCE_DIR}/include
                                           ../vendor/googletest/googlemock/include)
target_link_libraries(cpp-test PUBLIC gtest gmock pid_lib)
