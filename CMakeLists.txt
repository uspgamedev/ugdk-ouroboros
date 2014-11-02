cmake_minimum_required (VERSION 2.8.11)
# 2.8.11 for target_include_directories

project (ugdk-ouroboros CXX C)

########################################

if(NOT ${CMAKE_CURRENT_SOURCE_DIR} STREQUAL ${CMAKE_CURRENT_BINARY_DIR})
    # Don't polute the git repository with the generated files for out-of-source builds
    file(WRITE ${CMAKE_CURRENT_BINARY_DIR}/.gitignore "*")
endif()

########################################

find_package(Ouroboros COMPONENTS Lua Python)

if(TARGET opwig-lua)
    message("OH YEAH FOUND opwig-lua")
else()
    message("SO SAD")
endif()
