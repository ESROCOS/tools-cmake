cmake_minimum_required(VERSION 2.6)
set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/modules")
include(${CMAKE_CURRENT_SOURCE_DIR}/modules/Sargon.cmake)

configure_file(modules/sargon-config.cmake.in sargon-config.cmake @ONLY)
install(FILES
    modules/FindBoost.cmake
    modules/FindGem.cmake
    modules/FindNumpy.cmake
    modules/FindRuby.cmake
    modules/FindSISL.cmake
    modules/ListMacros.cmake
    modules/PythonBind.cmake
    modules/PythonInstallPath.cmake
    modules/Sargon.cmake
    modules/SargonRuby.cmake
    ${CMAKE_CURRENT_BINARY_DIR}/sargon-config.cmake
    DESTINATION share/sargon/cmake)

