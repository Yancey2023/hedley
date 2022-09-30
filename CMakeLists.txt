cmake_minimum_required(3.1)
project(hedley)
include(CTest)
add_library(hedley INTERFACE include/hedley.h)
target_include_directories(hedley INTERFACE include)

if(HEDLEY_TESTING AND BUILD_TESTING)
  add_subdirectory(test)
endif()
