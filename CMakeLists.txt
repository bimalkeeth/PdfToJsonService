cmake_minimum_required(VERSION 3.14)
project(PdfToJsonService)

set(CMAKE_CXX_STANDARD 14)
set(cpprestsdk_DIR /usr/lib/${CMAKE_LIBRARY_ARCHITECTURE}/cmake/)
include_directories("/usr/lib/x86_64-linux-gnu")
find_package(cpprestsdk REQUIRED NAMES cpprestsdk cpprest)
add_executable(untitled8 main.cpp)
target_link_libraries(untitled8 PRIVATE cpprestsdk::cpprest)