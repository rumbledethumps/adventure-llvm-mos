cmake_minimum_required(VERSION 3.18)

add_subdirectory(tools)

set(LLVM_MOS_PLATFORM rp6502)
find_package(llvm-mos-sdk REQUIRED)

project(ADVENT4 C ASM)

add_executable(advent)
rp6502_executable(advent)
target_include_directories(advent PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/src
)
target_sources(advent PRIVATE
    src/err.c
    troglobit/src/advent.c
    troglobit/src/database.c
    troglobit/src/english.c
    troglobit/src/itverb.c
    troglobit/src/turn.c
    troglobit/src/verb.c
)
