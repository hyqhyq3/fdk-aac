project(fdk-aac)

set(FDK_LIBRARIES 
	libAACdec
	libAACenc
	libFDK
	libMpegTPDec
	libMpegTPEnc
	libPCMutils
	libSBRdec
	libSBRenc
	libSYS)

set(INCLUDE_DIRS)
foreach(MODULE ${FDK_LIBRARIES})
	list(APPEND INCLUDE_DIRS ${MODULE}/include)
endforeach()
include_directories(${INCLUDE_DIRS})

foreach(MODULE ${FDK_LIBRARIES})
	add_subdirectory(${MODULE})
endforeach()
