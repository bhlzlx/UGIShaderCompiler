project( ShaderCompiler )

include_directories( 
    ${CMAKE_SOURCE_DIR}/thirdparty/CMAssetsManage/inc
    ${CMAKE_SOURCE_DIR}/thirdparty/CMCore/inc
    ${CMAKE_SOURCE_DIR}/thirdparty/include
    ${CMAKE_SOURCE_DIR}/thirdparty
    ${CMAKE_SOURCE_DIR}/thirdparty/spirv-cross/
    ${CMAKE_SOURCE_DIR}/source
)

link_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/lib
)

add_executable( ShaderCompiler 
    ${CMAKE_CURRENT_SOURCE_DIR}/shaderCompilerMain.cpp
)

target_link_libraries( ShaderCompiler 
    CMUtil
    CMAssetsManage
    CMCore
    CMPlatform
    glslang
    OSDependent
    OGLCompiler
    SPIRV
    spirv-cross-core
)

