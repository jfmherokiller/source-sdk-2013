add_library(raytrace STATIC
        trace3.cpp
        raytrace.cpp
        trace2.cpp
        )
target_compile_options(raytrace PRIVATE
        #        -c
        #        -Qunused-arguments
        -x c++
        -arch i386
        #        -fmessage-length=137
        #        -fmacro-backtrace-limit=0
        #        -fcolor-diagnostics
        -std=gnu++11
        #        -Wno-trigraphs
        #        -fpascal-strings
        -O0
        #        -Wno-missing-field-initializers
        #        -Wno-missing-prototypes
        #        -Wno-return-type
        #        -Wno-non-virtual-dtor
        #        -Wno-overloaded-virtual
        #        -Wno-exit-time-destructors
        #        -Wno-missing-braces
        #        -Wparentheses
        #        -Wswitch
        #        -Wno-unused-function
        #        -Wno-unused-label
        #        -Wno-unused-parameter
        #        -Wno-unused-variable
        #        -Wunused-value
        #        -Wno-empty-body
        #        -Wno-uninitialized
        #        -Wno-unknown-pragmas
        #        -Wno-shadow
        #        -Wno-four-char-constants
        #        -Wno-conversion
        #        -Wno-constant-conversion
        #        -Wno-int-conversion
        #        -Wno-bool-conversion
        #        -Wno-enum-conversion
        #        -Wno-shorten-64-to-32
        #        -Wno-newline-eof
        #        -Wno-c++11-extensions
        -fasm-blocks
        -ffast-math
        -fstrict-aliasing
        #        -Wdeprecated-declarations
        #        -Wno-invalid-offsetof
        -mmacosx-version-min=10.5
        -g
        -fvisibility=hidden
        -fvisibility-inlines-hidden
        #        -Wno-sign-conversion
        #        -Wno-infinite-recursion
        #        -Wno-move
        #        -Wno-deprecated-writable-strings
        #        -Wno-switch-enum
        #        -Wno-switch
        #        -Wno-unused-value
        #        -Wno-parentheses
        #        -Wno-logical-op-parentheses
        -Wno-c++11-narrowing
        #        -F${CMAKE_SOURCE_DIR}/build/Debug

        -UPROTECTED_THINGS_ENABLE
        -ftemplate-depth=512
        #        --serialize-diagnostics
        )
target_compile_definitions(raytrace PRIVATE
        OSX
        FORCE_QUICKTIME
        DX_TO_GL_ABSTRACTION
        _DLL_EXT=.dylib
        NO_MALLOC_OVERRIDE=1
        POSIX
        QUICKTIME_VIDEO
        GNUC
        USE_SDL
        VPC
        _OSX
        _POSIX=1
        FRAME_POINTER_OMISSION_DISABLED
        FD_SETSIZE=10240
        VPCGAME=hl2mp
        DEBUG
        PROJECTDIR=${CMAKE_SOURCE_DIR}/vgui2/vgui_controls
        _DARWIN_UNLIMITED_SELECT
        PNG_NO_PEDANTIC_WARNINGS
        -DCOMPILER_GCC
        OVERRIDE_V_DEFINES
        DEV_BUILD
        CPP11_NO_LIBCXX
        SOURCE1=1
        _EXTERNAL_DLL_EXT=.dylib
        VPROF_LEVEL=1
        VPCGAMECAPS=HL2MP
        NO_HOOK_MALLOC=1
        GL_GLEXT_PROTOTYPES
        _DEBUG
        RAD_TELEMETRY_DISABLED
        )
target_include_directories(raytrace PRIVATE
        ${CMAKE_SOURCE_DIR}/common
        ${CMAKE_SOURCE_DIR}/public
        ${CMAKE_SOURCE_DIR}/public/tier0
        ${CMAKE_SOURCE_DIR}/public/tier1
        ${CMAKE_SOURCE_DIR}/thirdparty/SDL2
        ${CMAKE_SOURCE_DIR}/utils/common
        ${CMAKE_SOURCE_DIR}/build/Debug/include
        ${CMAKE_SOURCE_DIR}/build/everything.build/Debug/raytrace.build/DerivedSources/i386
        ${CMAKE_SOURCE_DIR}/build/everything.build/Debug/raytrace.build/DerivedSources
        )
target_include_directories(raytrace SYSTEM PRIVATE
        )