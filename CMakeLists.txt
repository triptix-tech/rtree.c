cmake_minimum_required(VERSION 3.20)
project(rtree.c)

add_library(rtree rtree.c)
target_include_directories(rtree PUBLIC .)
set_target_properties(rtree PROPERTIES LINKER_LANGUAGE C)

if (MSVC)
    set_source_files_properties(rtree.c PROPERTIES LANGUAGE CXX)
    target_compile_features(rtree PRIVATE cxx_std_23)
endif()