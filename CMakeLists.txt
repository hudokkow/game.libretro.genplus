cmake_minimum_required(VERSION 3.1)
project(game.libretro.genplus)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-genplus REQUIRED)

set(DEPLIBS genplus)
set(GENPLUS_CUSTOM_BINARY ${GENPLUS_LIB}
                          ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} GENPLUS DEPLIBS)
