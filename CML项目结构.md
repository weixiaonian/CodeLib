Lib1.h
Lib1.cpp
add_library(lib1 STATIC
    sources/lib1.cpp
)
target_include_directories(lib1 PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
Lib2.h
Lib2.cpp
add_library(lib2 STATIC
    sources/lib2.cpp
)
target_include_directories(lib2 PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
add_subdirectory(库1)
add_subdirectory(库2)
cmake_minimum_required(VERSION 3.10)
project(项目名)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
add_subdirectory(libs)
add_subdirectory(program)
add_executable(my_program
    sources/main.cpp
    sources/class.cpp
)
target_include_directories(my_program PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
target_link_libraries(my_program PRIVATE
    lib1
    lib2
)
Main.cpp
Class.cpp
Class.h
CMAKE_LIBRARY_OUTPUT_DIRECTORY
动态库输出目录
CMAKE_ARCHIVE_OUTPUT_DIRECTORY
静态库输出目录
add_subdirectory
添加子目录
CMAKE_BINARY_DIR
构建树的顶层目录（build）
add_library
添加名为（）的库
STATIC
静态
动态
SHARED
target_link_libraries
目标头文件搜索路径
CMAKE_CURRENT_SOURCE_DIR
当前CML所在路径
add_executable
创建可执行程序
target_link_libraries
将目标链接库
add_subdirectory(文件夹名)
add_library(库名 库的类型
   相较于当前CML路径/源文件
)
target_include_directories(库名 PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
add_executable(程序名
    sources/main.cpp
    sources/lass.cpp
)
target_include_directories(程序名 PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
target_link_libraries(程序名 PRIVATE
    lib1
    lib2
)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
生成配置文件

CMAKE_LIBRARY_OUTPUT_DIRECTORY --> 动态库输出目录
CMAKE_ARCHIVE_OUTPUT_DIRECTORY --> 静态库输出目录
add_subdirectory --> 添加子目录
CMAKE_BINARY_DIR --> 构建树的顶层目录（build）
add_library --> 添加名为（）的库
STATIC --> 静态
SHARED --> 动态
target_link_libraries --> 目标头文件搜索路径
CMAKE_CURRENT_SOURCE_DIR --> 当前CML所在路径
add_executable --> 创建可执行程序
target_link_libraries --> 将目标链接库
set(CMAKE_EXPORT_COMPILE_COMMANDS ON) --> 生成配置文件
