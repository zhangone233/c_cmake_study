# 添加一个库，库名为 sum 的静态库，源文件是 sum/sum.c
add_library(sum STATIC sum/sum.c)

# 将 sum 库与 lib 目录进行链接
target_link_directories(sum PUBLIC ${CMAKE_CURRENT_LIST_DIR})
