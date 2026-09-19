cmake_minimum_required(VERSION 3.20)

project(lesson01 C)

add_library(hello STATIC
    hello.c
)
target_include_directories(hello PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include    
)
add_executable(main
    main.c
)
target_link_libraries(main PRIVATE hello)