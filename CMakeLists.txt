cmake_minimum_required (VERSION 3.21)
project ("ci-sample"
    VERSION 0.0.0
    DESCRIPTION "Usage of github actions with vcpkg and protobuf"
    LANGUAGES CXX)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")

enable_testing()
add_subdirectory ("external")
add_subdirectory ("model")
add_subdirectory ("test")