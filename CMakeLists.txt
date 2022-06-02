cmake_minimum_required (VERSION 3.16)

project (urdl)

file(GLOB URDL_SOURCES
     "include/*.hpp"
     "include/*.ipp"
     "src/*.cpp"
)

set(URDL_PUBLIC_INCLUDE_HEADERS ${PROJECT_SOURCE_DIR}/include PARENT_SCOPE)

include (${CMAKE_SOURCE_DIR}/${DEPS_BUILD_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

include_directories("include")

add_library (${PROJECT_NAME} STATIC
             ${URDL_SOURCES}
)
