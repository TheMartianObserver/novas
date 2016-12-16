cmake_minimum_required(VERSION 3.6)
project(novas)

set(NOVAS_LIB_SRCS
    src/novas.c
    src/novascon.c
    src/nutation.c
    src/solsys3.c
    src/readeph0.c)

add_library(novas ${NOVAS_LIB_SRCS})
target_include_directories(novas SYSTEM PUBLIC ${CMAKE_CURRENT_LIST_DIR}/src)
