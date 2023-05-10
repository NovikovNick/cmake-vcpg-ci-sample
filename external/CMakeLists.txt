add_library(ggpo STATIC IMPORTED GLOBAL)
add_library (ggpo::ggpo ALIAS ggpo)
target_include_directories(ggpo INTERFACE ggpo/src/include)
set_target_properties(ggpo 
    PROPERTIES 
        LINKER_LANGUAGE CXX
        IMPORTED_LOCATION ${CMAKE_SOURCE_DIR}/external/ggpo/build/lib/x64/${CMAKE_BUILD_TYPE}/GGPO.lib)