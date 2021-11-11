cmake_minimum_required(VERSION 3.16)

project(PIPEFISH VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


include_directories(.)

set(CMAKE_CXX_FLAGS "-O2 -Werror -Wall -Wextra -fpic")
#set(CMAKE_CXX_FLAGS_DEBUG "-g")
#set(CMAKE_CXX_FLAGS_RELWITHDEBINFO "-g")
#set(CMAKE_CXX_FLAGS_RELEASE "-DNDEBUG")

# Install inside the build directory.
set(CMAKE_INSTALL_PREFIX ${CMAKE_BINARY_DIR}/install)

#if (NOT CMAKE_BUILD_TYPE)
#    set(CMAKE_BUILD_TYPE Release)
#endif()

# Do not strip RPATH during installation
#set(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)
#set(CMAKE_INSTALL_RPATH "${CMAKE_BINARY_DIR}/systemc_dir/lib")

#enable_testing()

add_subdirectory(src/pipefish-gui)
#add_subdirectory(test)
#add_subdirectory(doc)

#message(STATUS "Build type: ${CMAKE_BUILD_TYPE}")
