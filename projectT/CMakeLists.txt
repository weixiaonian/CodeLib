cmake_minimum_required(VERSION 4.0)
project(test)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY 
${CMAKE_BINARY_DIR}/bin)#生成的静态库保存在构建目录bin下
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY 
${CMAKE_BINARY_DIR}/bin)#生成的动态库保存在构建目录bin下
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY 
${CMAKE_BINARY_DIR}/bin)#生成的程序保存在构建目录bin下

add_subdirectory(lib)
add_subdirectory(program)