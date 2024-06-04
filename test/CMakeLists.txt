cmake_minimum_required(VERSION 3.20)

# BUILD_TESTING variable is created by include(CTest)
# It is set to ON by default
if(BUILD_TESTING)
  add_executable(module_test test.cpp)
  target_link_libraries(module_test PRIVATE GTest::gtest_main)

  include(GoogleTest)
  # Finds all the Google tests associated with the executable
  gtest_discover_tests(module_test)
endif()
