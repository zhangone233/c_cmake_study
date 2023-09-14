# set(): 可用来设置变量值。 取用变量时可以 ${变量名}
# 在 IF 中直接使用变量名即可
set(PROJECT_CMAKE_VERSION 3.25) # 定义一个名为 PROJECT_CMAKE_VERSION 的变量，其值为：3.25

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

set(CMAKE_BUILD_TYPE Release)
#set(CMAKE_BINARY_DIR /dist)

set(MY_BUILD_DIR "${CMAKE_BINARY_DIR}/dist")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${MY_BUILD_DIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${MY_BUILD_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${MY_BUILD_DIR})

# cmake_minimum_required()：指定CMake的最小版本
cmake_minimum_required(VERSION ${PROJECT_CMAKE_VERSION}) # 取变量，设置CMake的版本为3.25

# project(): 指定项目名称及版本号
project(c_project VERSION 0.0.1) # 项目名称为 c_project, 版本号为 0.0.1

add_subdirectory(lib)
add_subdirectory(tests)

# add_executable(): 添加可执行性文件 params1: 可执行文件名称 params2: 编译所需文件
#add_executable(main main.c) # 编译 main.c 源文件，产物名为 main 的可执行文件



