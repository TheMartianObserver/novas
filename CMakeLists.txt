project(NOVAS)
cmake_minimum_required(VERSION 2.8)

# Build using solsys1

set(NOVAS_LIB_SRCS
    src/eph_manager.c
    src/novas.c
    src/novascon.c
    src/nutation.c
    src/readeph0.c
    src/solsys1.c)

add_library(novas ${NOVAS_LIB_SRCS})

add_executable(example src/example.c)
target_link_libraries(example novas)

