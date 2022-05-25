cmake_minimum_required(VERSION 3.21)
project(bluez_binding C)

set(CMAKE_C_STANDARD 99)

find_package(PkgConfig REQUIRED)

pkg_search_module(GLIB REQUIRED glib-2.0)
pkg_search_module(GIO REQUIRED gio-2.0)
pkg_search_module(GIOUNIX REQUIRED gio-unix-2.0)

include_directories(
        ${GLIB_INCLUDE_DIRS}
        ${GIO_INCLUDE_DIRS}
        ${GIOUNIX_INCLUDE_DIRS}
)

add_library(bluez_binding SHARED generated-code.c)

target_link_libraries(bluez_binding ${GLIB_LIBRARIES} ${GIO_LIBRARIES} ${GIOUNIX_LIBRARIES})
