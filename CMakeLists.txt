cmake_minimum_required(VERSION 3.20)

project(
    PicoStep
    VERSION 0.1.0
    LANGUAGES CXX
)

add_library(picostep INTERFACE)

target_include_directories(
    picostep
    INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:include>
)

target_compile_features(
    picostep
    INTERFACE
        cxx_std_20
)

option(PICOSTEP_BUILD_EXAMPLES "Build PicoStep examples" OFF)
option(PICOSTEP_BUILD_TESTS "Build PicoStep tests" OFF)

if(PICOSTEP_BUILD_EXAMPLES)
    add_subdirectory(examples)
endif()

if(PICOSTEP_BUILD_TESTS)
    enable_testing()
    add_subdirectory(tests)
endif()