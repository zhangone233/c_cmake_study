add_executable(test test.c)

target_link_libraries(test PRIVATE sum)

#target_link_directories(test PRIVATE ${CMAKE_SOURCE_DIR}/lib/sum)

#TARGET_LINK_DIRECTORIES(test PRIVATE ../lib/sum)

# 将自定义库头文件的所在目录，包含在可执行目标 test 的include查找范围内。
target_include_directories(test PRIVATE ../lib/sum)
