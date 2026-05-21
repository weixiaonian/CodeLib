add_executable(test)

target_sources(test PRIVATE
sources/main.cpp
sources/Proclass.cpp)

target_include_directories(test PRIVATE
${CMAKE_CURRENT_BINARY_DIR}/include)

target_link_libraries(test PRIVATE
mylib)