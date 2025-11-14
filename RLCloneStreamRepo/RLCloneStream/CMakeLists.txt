
cmake_minimum_required(VERSION 3.10)
project(RLCloneStream)

set(CMAKE_SYSTEM_NAME Windows)
set(CMAKE_CXX_COMPILER x86_64-w64-mingw32-g++)
set(CMAKE_CXX_STANDARD 17)

include_directories(
    ${CMAKE_SOURCE_DIR}/../BakkesModSDK/include
)

link_directories(
    ${CMAKE_SOURCE_DIR}/../BakkesModSDK/lib
)

add_library(RLCloneStream SHARED
    RLCloneStream.cpp
    RLCloneStream.h
)

target_link_libraries(RLCloneStream ws2_32)
