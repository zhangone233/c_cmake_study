add_executable(test test.c)

target_link_libraries(test PRIVATE sum)

target_link_directories(test PUBLIC ${CMAKE_SOURCE_DIR}/lib/sum)
