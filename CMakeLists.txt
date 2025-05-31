cmake_minimum_required(VERSION 3.28.3)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(apps)

add_subdirectory(formatter_lib)

add_subdirectory(formatter_ex_lib)

add_subdirectory(solver_lib)

add_subdirectory(hello_world_application)

add_subdirectory(solver_application)

set(CPACK_PACKAGE_NAME "solver")
set(CPACK_PACKAGE_VERSION "0.0.1")

set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Nikpop228")

set(CPACK_RPM_PACKAGE_NAME "solver")
set(CPACK_NSIS_PACKAGE_NAME "solver")

set(CPACK_GENERATOR DEB RPM WIX DragNDrop)

include(CPack)