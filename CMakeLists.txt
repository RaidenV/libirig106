
cmake_minimum_required(VERSION 3.12)

project(libirig106
    VERSION 0.2.0
    LANGUAGES C CXX)

# Build flags
set(CMAKE_BUILD_TYPE RelWithDebInfo)

# Library
include_directories(include)
file(GLOB SOURCES "src/*.c")
add_library(irig106 SHARED STATIC ${SOURCES})
set_property(TARGET irig106 PROPERTY C_STANDARD 99)
set_property(TARGET irig106 PROPERTY POSITION_INDEPENDENT_CODE ON)
install(TARGETS irig106 DESTINATION ${PROJECT_SOURCE_DIR})
