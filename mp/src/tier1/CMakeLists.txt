add_library(tier1 STATIC
        snappy.cpp
        checksum_sha1.cpp
        ilocalize.cpp
        commandbuffer.cpp
        utlbinaryblock.cpp
        utlbuffer.cpp
        ../utils/lzma/C/LzmaDec.c
        byteswap.cpp
        mempool.cpp
        kvpacker.cpp
        rangecheckedvar.cpp
        snappy-stubs-internal.cpp
        NetAdr.cpp
        strtools.cpp
        snappy-sinksource.cpp
        KeyValues.cpp
        processor_detect_linux.cpp
        lzmaDecoder.cpp
        utlbufferutil.cpp
        sparsematrix.cpp
        uniqueid.cpp
        diff.cpp
        tier1.cpp
        utlsymbol.cpp
        characterset.cpp
        memstack.cpp
        checksum_crc.cpp
        newbitbuf.cpp
        strtools_unicode.cpp
        checksum_md5.cpp
        splitstring.cpp
        interface.cpp
        tokenreader.cpp
        convar.cpp
        generichash.cpp
        stringpool.cpp
        bitbuf.cpp
        reliabletimer.cpp
        utlstring.cpp
        datamanager.cpp
        )
target_compile_options(tier1 PRIVATE
#        -c
#        -Qunused-arguments
#        -x c++
#        -arch i386
#        -fmessage-length=137
#        -fmacro-backtrace-limit=0
#        -fcolor-diagnostics
#        -std=gnu++11
#        -Wno-trigraphs
#        -fpascal-strings
#        -O0
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
#        -fasm-blocks
#        -ffast-math
#        -fstrict-aliasing
#        -Wdeprecated-declarations
#        -Wno-invalid-offsetof
#        -mmacosx-version-min=10.5
#        -g
#        -fvisibility=hidden
#        -fvisibility-inlines-hidden
#        -Wno-sign-conversion
#        -Wno-infinite-recursion
#        -Wno-move
#        -Wno-deprecated-writable-strings
#        -Wno-switch-enum
#        -Wno-switch
#        -Wno-unused-value
#        -Wno-parentheses
#        -Wno-logical-op-parentheses
#        -Wno-c++11-narrowing
#        -F${CMAKE_SOURCE_DIR}/build/Debug
#        -Usprintf
#        -Ustrncpy
#        -UPROTECTED_THINGS_ENABLE
#        -ftemplate-depth=512
#        --serialize-diagnostics
        )
target_compile_definitions(tier1 PRIVATE
        FORCE_QUICKTIME
        DX_TO_GL_ABSTRACTION
        _DLL_EXT=.dylib
        TIER1_STATIC_LIB
        POSIX
        QUICKTIME_VIDEO
        VPC
        _OSX
        _POSIX=1
        VPCGAME=hl2mp
        PROJECTDIR=${CMAKE_SOURCE_DIR}/tier1
        _DARWIN_UNLIMITED_SELECT
        PNG_NO_PEDANTIC_WARNINGS
        COMPILER_GCC
        OVERRIDE_V_DEFINES
        DEV_BUILD
        CPP11_NO_LIBCXX
        _EXTERNAL_DLL_EXT=.dylib
        VPROF_LEVEL=1
        NO_HOOK_MALLOC=1
        RAD_TELEMETRY_DISABLED
        FRAME_POINTER_OMISSION_DISABLED
        SOURCE1=1
        NO_MALLOC_OVERRIDE=1
        DEBUG
        USE_SDL
        FD_SETSIZE=10240
        OSX
        _DEBUG
        GNUC
        VPCGAMECAPS=HL2MP
        GL_GLEXT_PROTOTYPES
        )
target_include_directories(tier1 PRIVATE
        ${CMAKE_SOURCE_DIR}/common
        ${CMAKE_SOURCE_DIR}/public
        ${CMAKE_SOURCE_DIR}/public/tier0
        ${CMAKE_SOURCE_DIR}/public/tier1
        ${CMAKE_SOURCE_DIR}/thirdparty/SDL2
        ${CMAKE_SOURCE_DIR}/build/Debug/include
        /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.12.sdk/usr/include/malloc
        ${CMAKE_SOURCE_DIR}/build/everything.build/Debug/tier1.build/DerivedSources/i386
        ${CMAKE_SOURCE_DIR}/build/everything.build/Debug/tier1.build/DerivedSources
        )
target_include_directories(tier1 SYSTEM PRIVATE
        )