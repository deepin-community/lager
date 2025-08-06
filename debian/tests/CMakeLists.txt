cmake_minimum_required(VERSION 3.20)
project(lager-tests)

enable_testing()

find_package(Lager REQUIRED)
# aliases used by the examples
add_library(lager-example ALIAS lager)
add_library(lager-debugger-example ALIAS lager)

find_package(SDL2_ttf REQUIRED)
set(SDL2_TTF_LIBRARIES SDL2_ttf::SDL2_ttf)

set(lager_BUILD_DEBUGGER_EXAMPLES TRUE)

add_subdirectory(examples)
