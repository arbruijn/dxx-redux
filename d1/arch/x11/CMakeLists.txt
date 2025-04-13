add_library(arch_x11 STATIC
    messagebox.c
    x11messagebox.c
    )

include_directories(${CMAKE_SOURCE_DIR}/include ${CMAKE_SOURCE_DIR}/arch/include ${CMAKE_SOURCE_DIR}/main)

find_package(X11)

target_include_directories(arch_x11 PUBLIC ${SDL_INCLUDE_DIR} ${X11_INCLUDE_DIR})
