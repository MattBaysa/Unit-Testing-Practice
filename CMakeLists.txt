cmake_minimum_required(VERSION 3.20)
project(unitTestTest)

set(CMAKE_CXX_STANDARD 14)

# 'lib' is the folder with Google Test sources
add_subdirectory(googletest-main)
include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

# 'Google_Tests_run' is the target name
# 'test1.cpp tests2.cpp' are source files with tests
add_executable(unitTestTest triangleTest.cpp triangle.cpp)
target_link_libraries(unitTestTest gtest gtest_main)
