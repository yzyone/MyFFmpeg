cmake_minimum_required(VERSION 3.14)
project(myffmpeg)

set(CMAKE_CXX_STANDARD 11)

MESSAGE(STATUS "other platform: ${CMAKE_SYSTEM_NAME}")

# 添加头文件
include_directories(
        ${CMAKE_CURRENT_SOURCE_DIR}/include
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libavcodec
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libavdevice
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libavfilter
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libavformat
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libavutil
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libpostproc
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libswresample
        #${CMAKE_CURRENT_SOURCE_DIR}/include/libswscale
)

link_directories(
        ${CMAKE_CURRENT_SOURCE_DIR}/lib
)

link_libraries(
        avcodec
        avdevice
        avfilter
        avformat
        avutil
        swresample
        swscale
)

add_executable(
        CGSaveFile
        CGSaveFile.cpp
)