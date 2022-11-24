cmake_minimum_required(VERSION 3.0.0)
project(binance-api VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(binance-api src/main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

find_package(fmt CONFIG REQUIRED)
target_link_libraries(binance-api PRIVATE fmt::fmt)