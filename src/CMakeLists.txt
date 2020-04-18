add_executable(opusinfo opusinfo.c
   picture.c
   info_opus.c
   opus_header.c
   ../share/getopt.c 
   ../win32/unicode_support.c
)
target_compile_options(opusinfo PRIVATE -DOPUSTOOLS)
target_link_libraries(opusinfo PRIVATE ogg)

add_executable(opusdec opusdec.c
   opus_header.c
   diag_range.c
   wav_io.c
   wave_out.c
   resample.c
   ../share/getopt.c 
   ../share/getopt1.c 
   ../win32/unicode_support.c
)
target_compile_options(opusdec PRIVATE -DRANDOM_PREFIX=opustools -DOUTSIDE_SPEEX -DRESAMPLE_FULL_SINC_TABLE)
target_link_libraries(opusdec PRIVATE opusfile Winmm)

add_executable(opusenc opusenc.c
   picture.c
   audio-in.c
   opus_header.c
   diag_range.c
   resample.c
   flac.c
   ../share/getopt.c 
   ../share/getopt1.c 
   ../win32/unicode_support.c
)
target_link_libraries(opusenc PRIVATE libopusenc ogg)
