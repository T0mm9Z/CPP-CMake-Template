cmake_minimum_required(VERSION 3.0)
project(cmake_template)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O3")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})
set(SRC_DIR ${PROJECT_SOURCE_DIR}/src)
set(INC_DIR ${PROJECT_SOURCE_DIR}/include)
set(BIN_DIR ${PROJECT_SOURCE_DIR}/bin)
set(LIB_DIR ${PROJECT_SOURCE_DIR}/lib)

message("Source Dir: " ${SRC_DIR})
message("Current Binary Dir: " ${CMAKE_CURRENT_BINARY_DIR})
add_subdirectory(${SRC_DIR})

# add_custom_command(
#         TARGET ${PROJECT_NAME}  POST_BUILD
#         COMMAND ${CMAKE_COMMAND} -E copy
#                 ${CMAKE_CURRENT_BINARY_DIR}/cmake_templ_main
#                 ${BIN_DIR}/cmake_templ_main)