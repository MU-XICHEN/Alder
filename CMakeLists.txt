cmake_minimum_required(VERSION 3.20)
project(Alder LANGUAGES CXX)

# Engine library for application targets.
add_library(Engine STATIC Engine/src/Version.cpp)

# Public headers use the <Alder/...> include prefix.
target_include_directories(Engine PUBLIC Engine/include)
target_compile_features(Engine PRIVATE cxx_std_20)
set_target_properties(Engine PROPERTIES CXX_EXTENSIONS OFF)

# Console app for checking the engine version.
add_executable(Alder main.cpp)
target_link_libraries(Alder PRIVATE Engine)
target_compile_features(Alder PRIVATE cxx_std_20)
set_target_properties(Alder PROPERTIES CXX_EXTENSIONS OFF)
