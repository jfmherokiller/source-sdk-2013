cmake_minimum_required(VERSION 3.0)
project(hl2mp)

add_definitions(-x c++ -arch i386 -fasm-blocks
        -ffast-math -fstrict-aliasing -Usprintf
        -Ustrncpy
        -Wno-inconsistent-missing-override -Wno-narrowing
        -Wno-dangling-else
        -ftemplate-depth=512 -mmacosx-version-min=10.5 -fvisibility=hidden
        -fvisibility-inlines-hidden -fpascal-strings -std=gnu++11
        )
add_subdirectory(tier1)
add_subdirectory(mathlib)

add_subdirectory(materialsystem)

add_subdirectory(vgui2)
add_subdirectory(utils/serverplugin_sample)
add_subdirectory(game/client)
add_subdirectory(game/server)
add_subdirectory(raytrace)