include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/Core/inc
    ${CMAKE_CURRENT_SOURCE_DIR}/Platform/inc
    ${CMAKE_CURRENT_SOURCE_DIR}/Util/inc
    ${CMAKE_CURRENT_SOURCE_DIR}/AssetsManage/inc
    ${CMAKE_CURRENT_SOURCE_DIR}/MathGeoLib/src
    ${CMAKE_CURRENT_SOURCE_DIR}/
)


use_cm_module(Core)
use_cm_module(Platform)
use_cm_module(Util)
use_cm_module(AssetsManage)

add_subdirectory( MathGeoLib )

add_subdirectory( glslang )
add_subdirectory( spirv-cross )