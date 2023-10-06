cmake_minimum_required(VERSION 3.20)
project(rtree.c LANGUAGES C)

add_library(rtree rtree.c)
target_include_directories(rtree PUBLIC .)