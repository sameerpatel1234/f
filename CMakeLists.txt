CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

PROJECT(mcmap LANGUAGES CXX VERSION 3.0.1)

SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

OPTION(DEBUG_BUILD "Debug build" OFF)

FIND_PACKAGE(OpenMP)
FIND_PACKAGE(PNG REQUIRED)
FIND_PACKAGE(ZLIB REQUIRED)
FIND_PACKAGE(GTest)

SET(CMAKE_CXX_STANDARD 17)
SET(CMAKE_CXX_STANDARD_REQUIRED ON)

INCLUDE_DIRECTORIES(src/include)

ADD_SUBDIRECTORY(src/include/fmt)
ADD_SUBDIRECTORY(scripts)
ADD_SUBDIRECTORY(src)
ADD_SUBDIRECTORY(tests)
