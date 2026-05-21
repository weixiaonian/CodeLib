cmake_minimum_required(VERSION 3.50)
project(test)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Debug" CACHE
    STRING "Build type" FORCE)
endif()
#xcrun --show-sdk-path 查找sdk路径
set(CMAKE_OSX_SYSROOT "/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk" CACHE PATH "")
set(CMAKE_CXX_STANDARD 20)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY 
${CMAKE_BINARY_DIR}/bin)#生成的静态库保存在构建目录bin下
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY 
${CMAKE_BINARY_DIR}/bin)#生成的动态库保存在构建目录bin下
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY 
${CMAKE_BINARY_DIR}/bin)#生成的程序保存在构建目录bin下

add_subdirectory(lib)
add_subdirectory(program)