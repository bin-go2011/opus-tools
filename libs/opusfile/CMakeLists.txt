add_library(opusfile src/opusfile.c
    src/http.c
    src/info.c
    src/internal.c    
    src/stream.c
    src/wincerts.c
)
target_include_directories(opusfile PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)
target_link_libraries(opusfile PUBLIC ogg opus)