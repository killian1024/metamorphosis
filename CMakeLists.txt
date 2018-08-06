cmake_minimum_required(VERSION 3.9)

project(metamorphosis)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/lib")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/bin")

set(SOURCE_FILES
        src/main.cpp
        src/program.cpp
        src/program.hpp
        src/base_name.hpp
        src/base_number.hpp
        src/file_target.hpp
        src/image_target.hpp
        src/base_number.cpp
        src/sort_policie.hpp
        src/file_target.cpp
        src/image_target.cpp
        )

add_executable(metamorphosis ${SOURCE_FILES})
target_link_libraries(metamorphosis -ljpeg -lpng -lspeed -lstdc++fs)
install(TARGETS metamorphosis DESTINATION bin)
