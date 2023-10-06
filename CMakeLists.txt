cmake_minimum_required(VERSION 3.1...3.5)
project(psp-stb)

add_library(psp-stb STATIC stb_image.c)
target_include_directories(psp-stb PUBLIC ${PROJECT_SOURCE_DIR})