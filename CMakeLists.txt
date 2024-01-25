include_guard(GLOBAL)
message("FATFS component is included.")

file(GLOB FATFS_SOURCE_FILES_LIST 
    "${CMAKE_CURRENT_LIST_DIR}/source/diskio.c"
    "${CMAKE_CURRENT_LIST_DIR}/source/ff_gen_drv.c"
    "${CMAKE_CURRENT_LIST_DIR}/source/ff.c"
    "${CMAKE_CURRENT_LIST_DIR}/source/ffunicode.c"
)

target_sources(${PROJECT_NAME} PRIVATE
	${FATFS_SOURCE_FILES_LIST}
)

target_include_directories(${PROJECT_NAME} PUBLIC 
    ${CMAKE_CURRENT_LIST_DIR}/source
)
