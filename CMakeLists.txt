cmake_minimum_required(VERSION "3.0.0")

#Set target output directory
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib") # set output directory for library targets
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

# add to CMakeCache
option(BUILD_SHARED_LIBS "True when building a shared library" True)

project("Foo")

add_subdirectory("foo") # add_subdirectory tells Cmake to goto ./foo and execute ./foo/CMakeLists.txt

add_subdirectory("examples")