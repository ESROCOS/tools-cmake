cmake_minimum_required(VERSION 2.6)
set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/modules")
include(${CMAKE_CURRENT_SOURCE_DIR}/modules/esrocos.cmake)

configure_file(modules/esrocos-config.cmake.in esrocos-config.cmake @ONLY)
install(FILES
    modules/FindBoost.cmake
    modules/FindGem.cmake
    modules/FindNumpy.cmake
    modules/FindRuby.cmake
    modules/FindSISL.cmake
    modules/ListMacros.cmake
    modules/PythonBind.cmake
    modules/PythonInstallPath.cmake
    modules/esrocos.cmake
    modules/esrocosRuby.cmake
    ${CMAKE_CURRENT_BINARY_DIR}/esrocos-config.cmake
    DESTINATION share/esrocos/cmake)

