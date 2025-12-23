add_library(inih INTERFACE)

target_sources(inih INTERFACE  ${CMAKE_CURRENT_SOURCE_DIR}/ini.c)


target_link_libraries(inih INTERFACE
        pico_stdlib
        )

# add the `binary` directory so that the generated headers are included in the project
#
target_include_directories(inih INTERFACE
	${CMAKE_CURRENT_SOURCE_DIR}
	${CMAKE_CURRENT_BINARY_DIR}
	)
