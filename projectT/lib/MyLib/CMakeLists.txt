add_library(mylib STATIC
sources/LibClass.cpp)

target_include_directories(mylib PUBLIC
${CMAKE_CURRENT_BINARY_DIR}/include)