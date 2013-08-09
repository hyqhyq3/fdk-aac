get_filename_component(LIBNAME ${CMAKE_CURRENT_SOURCE_DIR} NAME )
aux_source_directory(src ${LIBNAME}_SOURCES)
add_library(${LIBNAME} ${${LIBNAME}_SOURCES})

install(TARGETS ${LIBNAME} EXPORT fdk-aac DESTINATION lib)
install(DIRECTORY include/ DESTINATION include)