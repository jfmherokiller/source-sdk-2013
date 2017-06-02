cmake_minimum_required(VERSION 3.0)
project(hl2mp)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake")
find_package(iconv REQUIRED)
set(CMAKE_OSX_ARCHITECTURES i386)
add_definitions(-x c++ -fasm-blocks
        -ffast-math
        -fstrict-aliasing
        -Usprintf
        -Ustrncpy
        -mmacosx-version-min=10.5
        -ftemplate-depth=512
        -fvisibility=hidden
        -fvisibility-inlines-hidden
        -fpascal-strings
        -fmessage-length=0
        -fmacro-backtrace-limit=0
        -fdiagnostics-show-note-include-stack
        -std=gnu++11
        -Wno-inconsistent-missing-override
        -Wno-narrowing
        -Wno-dangling-else
        -Wno-null-dereference
        -Wno-unused-value
        -Wno-missing-field-initializers
        -Wno-missing-prototypes
        -Wno-return-type
        -Wno-non-virtual-dtor
        -Wno-overloaded-virtual
        -Wno-exit-time-destructors
        -Wno-missing-braces
        -Wparentheses
        -Wswitch
        -Wno-unused-function
        -Wno-unused-label
        -Wno-unused-parameter
        -Wno-unused-variable
        -Wunused-value
        -Wno-empty-body
        -Wno-uninitialized
        -Wno-unknown-pragmas
        -Wno-shadow
        -Wno-four-char-constants
        -Wno-conversion
        -Wno-constant-conversion
        -Wno-int-conversion
        -Wno-bool-conversion
        -Wno-enum-conversion
        -Wno-shorten-64-to-32
        -Wno-newline-eof
        -Wno-c++11-extensions
        -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.12.sdk
        )
add_subdirectory(tier1)
add_subdirectory(mathlib)

add_subdirectory(materialsystem)

add_subdirectory(vgui2)
add_subdirectory(utils/serverplugin_sample)
add_subdirectory(game/client)
add_subdirectory(game/server)
add_subdirectory(raytrace)