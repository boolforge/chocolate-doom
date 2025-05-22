cmake_minimum_required(VERSION 3.16)
project(ShooterVM LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Compiler flags
if(CMAKE_COMPILER_IS_GNUCC OR CMAKE_COMPILER_IS_CLANG)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror")
endif()

# Add more project configurations as needed
# For example, include directories
include_directories(include libosystem/include) # Assuming oSystem headers will be in libosystem/include

# Add subdirectories
add_subdirectory(src)
# add_subdirectory(plugins) # Will be added when plugins are being developed
# add_subdirectory(libosystem) # Will be added when oSystem is being integrated

message(STATUS "ShooterVM project configured")
message(STATUS "Compiler: ${CMAKE_CXX_COMPILER_ID} ${CMAKE_CXX_COMPILER_VERSION}")
message(STATUS "Standard: ${CMAKE_CXX_STANDARD}")
message(STATUS "Flags: ${CMAKE_CXX_FLAGS}")
