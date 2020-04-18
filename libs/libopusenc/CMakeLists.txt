add_library(libopusenc src/opusenc.c 
    src/ogg_packer.c 
    src/opus_header.c 
    src/picture.c 
    src/resample.c 
    src/unicode_support.c
)
target_compile_options(libopusenc PUBLIC -DRANDOM_PREFIX=opustools -DOUTSIDE_SPEEX)
target_include_directories(libopusenc PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)
target_link_libraries(libopusenc PUBLIC opus)
