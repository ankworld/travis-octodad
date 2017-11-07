cmake_minimal_required (VERSION 2.6)
project (travis-octodad)

# the version number.
set (travis-octodad_VERSION_MAJOR 1)
set (travis-octodad_VERSION_MINOR 0)

# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/TravisOctodadConfig.h.in"
  "${PROJECT_BINARY_DIR}/TravisOctodadConfig.h"
  )
 
# add the binary tree to the search path for include files
# so that we will find TravisOctodadConfig.h
include_directories("${PROJECT_BINARY_DIR}")

add_executable (travis-octodad main.cpp)
