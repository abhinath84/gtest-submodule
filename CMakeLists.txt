cmake_minimum_required(VERSION 3.20)

project(submodule
        VERSION 0.0.1
        DESCRIPTION "Setup googletest with git submodule"
        LANGUAGES CXX)

# Update the submodules here
include(cmake/UpdateSubmodule.cmake)
# Enable testing for this project
include(CTest)

# Add subdirectories with code
add_subdirectory(external)
add_subdirectory(test)
