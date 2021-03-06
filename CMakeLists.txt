# CMakeList.txt: 顶层 CMake 项目文件，在此处执行全局配置
# 并包含子项目。
#
cmake_minimum_required (VERSION 3.4)
project( UGI-ShaderCompiler )

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/thirdparty/CMCMakeModule )
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/UGICMakeModule )

set( WINDOW_SYSTEM Win32 )

message( "target platform : ${CMAKE_SYSTEM_NAME}")

set( SOLUTION_DIR ${CMAKE_CURRENT_SOURCE_DIR} )

link_directories(
    ${SOLUTION_DIR}/lib/${CMAKE_SYSTEM_NAME}/${TARGET_ARCH}
)

if( MSVC )
    set( THIRD_PART_LIB_DIR ${SOLUTION_DIR}/lib/${CMAKE_SYSTEM_NAME}/${TARGET_ARCH} )
endif()

include(use_cm_module)

include(outputPath)

add_subdirectory( thirdparty )

add_subdirectory( ShaderCompiler )
