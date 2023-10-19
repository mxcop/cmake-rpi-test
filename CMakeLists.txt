cmake_minimum_required(VERSION 3.15)
project(cmake-rpi-test)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)

# Create executable target
add_executable(main)
set_target_properties(main PROPERTIES OUTPUT_NAME ${CMAKE_PROJECT_NAME})

# Add header include directory
target_include_directories(main PRIVATE "src")

# Glob all source files
file(GLOB_RECURSE SOURCES
    "src/*.cpp"
)

# Add source files into target main
target_sources(main PRIVATE
    ${SOURCES}
)
