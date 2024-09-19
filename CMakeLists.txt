cmake_minimum_required(VERSION 3.21)

project(hedley
        VERSION 17.0.0
        DESCRIPTION "Header file designed to smooth over some platform-specific annoyances."
        HOMEPAGE_URL "https://github.com/Yancey2023/hedley"
        LANGUAGES CXX C)

add_library(hedley INTERFACE include/hedley.h)

target_include_directories(hedley INTERFACE include)

# Test
if (PROJECT_IS_TOP_LEVEL)
    include(CTest)
    add_subdirectory(test)
endif ()
