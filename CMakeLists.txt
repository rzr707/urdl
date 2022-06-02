cmake_minimum_required (VERSION 3.16)

project (urdl)
set (CMAKE_CXX_STANDARD 20)

file(GLOB URDL_SOURCES
     "include/*.hpp"
     "include/*.ipp"
     "src/*.cpp"
)

include (${CMAKE_SOURCE_DIR}/build/conanbuildinfo.cmake)
conan_basic_setup()

include_directories ("include")

add_library (${PROJECT_NAME} STATIC
             ${URDL_SOURCES}
)

target_link_libraries(${PROJECT_NAME} ${CONAN_LIBS} wsock32 ws2_32 user32 advapi32 gdi32)