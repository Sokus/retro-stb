cmake_minimum_required(VERSION 3.5...3.10)
project(retro-stb)

add_library(retro-stb STATIC src/stb_image.c)
target_include_directories(retro-stb PUBLIC ${PROJECT_SOURCE_DIR}/src)

