
add_library(server-plugin SHARED
        serverplugin_bot.cpp
        serverplugin_empty.cpp
        ../../public/tier0/memoverride.cpp
        )

target_compile_definitions(server-plugin PRIVATE
        FORCE_QUICKTIME
        DX_TO_GL_ABSTRACTION
        _DLL_EXT=.dylib
        POSIX
        QUICKTIME_VIDEO
        VPC
        _OSX
        _POSIX=1
        VPCGAME=hl2mp
        _MBCS
        PROJECTDIR=${CMAKE_SOURCE_DIR}/vgui2/vgui_controls
        _DARWIN_UNLIMITED_SELECT
        PNG_NO_PEDANTIC_WARNINGS
        COMPILER_GCC
        OVERRIDE_V_DEFINES
        DEV_BUILD
        CPP11_NO_LIBCXX
        _EXTERNAL_DLL_EXT=.dylib
        VPROF_LEVEL=1
        NO_HOOK_MALLOC=1
        serverplugin_emptyONLY
        RAD_TELEMETRY_DISABLED
        FRAME_POINTER_OMISSION_DISABLED
        SOURCE1=1
        NO_MALLOC_OVERRIDE=1
        DEBUG
        USE_SDL
        FD_SETSIZE=10240
        OSX
        _DEBUG
        DLLNAME=serverplugin_empty
        GNUC
        VPCGAMECAPS=HL2MP
        GL_GLEXT_PROTOTYPES
        )
target_include_directories(server-plugin PRIVATE
        ${CMAKE_SOURCE_DIR}/common
        ${CMAKE_SOURCE_DIR}/public
        ${CMAKE_SOURCE_DIR}/public/tier0
        ${CMAKE_SOURCE_DIR}/public/tier1
        ${CMAKE_SOURCE_DIR}/thirdparty/SDL2
        ${CMAKE_SOURCE_DIR}/game/server
        ${CMAKE_SOURCE_DIR}/game/shared
        ${CMAKE_SOURCE_DIR}/build/Debug/include
        ${CMAKE_SOURCE_DIR}/build/everything.build/Debug/serverplugin_empty.build/DerivedSources/i386
        ${CMAKE_SOURCE_DIR}/build/everything.build/Debug/serverplugin_empty.build/DerivedSources
        )
target_include_directories(server-plugin SYSTEM PRIVATE
        )