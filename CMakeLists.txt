cmake_minimum_required(VERSION 3.10)

# Set the project name
project(cc-bot)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Set the output directories
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/lib)

# Define source and include directories
set(SOURCE_DIR ${PROJECT_SOURCE_DIR}/src)
set(INCLUDE_DIR ${PROJECT_SOURCE_DIR}/inc)

# Add include directories
include_directories(${INCLUDE_DIR})

# Add source files
file(GLOB_RECURSE SOURCES "${SOURCE_DIR}/*.cc")

# Add the executable
add_executable(${PROJECT_NAME} ${SOURCES})

# Link libraries (placeholder for future use)
# target_link_libraries(${PROJECT_NAME} ${LIBRARIES})