cmake_minimum_required(VERSION 3.20)
project(Alder LANGUAGES CXX)

add_executable(Alder main.cpp)
target_compile_features(Alder PRIVATE cxx_std_20)
set_target_properties(Alder PROPERTIES CXX_EXTENSIONS OFF)
