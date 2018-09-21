cmake_minimum_required(VERSION 2.8)
project(sensor)
#aux_source_directory(. SRC_LIST)
#add_executable(${PROJECT_NAME} ${SRC_LIST})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
#set(CMAKE_CXX_STANDARD 11)

find_package(Qt5Core REQUIRED)

set(SOURCE_FILES main)
add_executable(sensor ${SOURCE_FILES})
qt5_use_modules(sensor Core SerialPort)
qt5_use_modules(sensor Widgets)
