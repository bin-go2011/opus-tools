add_executable(opusinfo opusinfo.c
   picture.c
   info_opus.c
   opus_header.c
   ../share/getopt.c 
   ../win32/unicode_support.c
)
target_link_libraries(opusinfo PRIVATE Ogg::Ogg)