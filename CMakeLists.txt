cmake_minimum_required(VERSION 3.14)
project(PdfToJsonService)

set(CMAKE_CXX_STANDARD 14)
set(cpprestsdk_DIR /usr/lib/${CMAKE_LIBRARY_ARCHITECTURE}/cmake/)
include_directories(src)
include_directories(/usr/lib/x86_64-linux-gnu
        src
        xpdf
        splash
        goo
        freetype.win32/lib
        freetype.win32/include
        fofi)
find_package(cpprestsdk REQUIRED NAMES cpprestsdk cpprest)
add_executable(PdfToJsonService main.cpp )
target_link_libraries(PdfToJsonService PRIVATE cpprestsdk::cpprest)