add_library(audio_bootloader_lib SHARED
	qpsk/packet_decoder.cc
	qpsk/packet_decoder.h
)

target_include_directories(audio_bootloader_lib
PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
)

target_link_libraries(audio_bootloader_lib
	PRIVATE
	stm_lib
)
