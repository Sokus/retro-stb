cmake_minimum_required(VERSION 3.1...3.5)
project(retro-stb)

if(3DS)
    add_library(retro-stb STATIC 3ds/stb_image.c)
    target_include_directories(retro-stb PUBLIC ${PROJECT_SOURCE_DIR}/3ds)
    target_link_libraries(retro-stb PRIVATE ${LIBCTRU_LIBRARIES})
    target_include_directories(retro-stb PRIVATE ${LIBCTRU_INCLUDE_DIRS})
else()
    add_library(retro-stb STATIC psp/stb_image.c)
    target_include_directories(retro-stb PUBLIC ${PROJECT_SOURCE_DIR}/psp)
endif()

