set(FILES "${CMAKE_CURRENT_SOURCE_DIR}/Hello.cpp")
set(SUBDIRECTORIES "")
set(RELATIVE_PATH "src/Foo") # relative to /foo

#loop to Add all subdirectories
foreach(VAR ${SUBDIRECTORIES}) # for each SUBDIRECTORIES, put it in VAR
	add_subdirectory(${VAR}) # then add VAR
endforeach()

if(FILES)
	#Add ${FILES} source files to target ${PROJECT_NAME}
	target_sources("${PROJECT_NAME}" PRIVATE ${FILES})

	#Install our source files into Desination ${CMAKE_INSTALL_PREFIX}/include
	install(FILES ${FILES} DESTINATION ${RELATIVE_PATH})
endif()