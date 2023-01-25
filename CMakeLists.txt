cmake_minimum_required(VERSION 3.2)
set(CMAKE_CXX_STANDARD 20)

# hunter module, keep up-to-date
include("cmake/HunterGate.cmake")
HunterGate(
    URL "https://github.com/cpp-pm/hunter/archive/v0.24.14.tar.gz"
    SHA1 "00901c19eefc02d24b16705b5f5a2b4f093a73fb"
)

project(PROJECTNAME)

# use add_subdirectory to add 3rd party lib
#add_subdirectory(third_party/lib)

# use hunter_add_package to add library, find_package to include it to cmake project
#hunter_add_package(Boost COMPONENTS program_options)
#find_package(Boost CONFIG REQUIRED program_options)

# define cpp files here
add_executable(
    ${PROJECT_NAME} 
    ${CMAKE_CURRENT_SOURCE_DIR}/sources/main.cpp
)

# define cpp files here
#add_library(
#    lib_name
#    ${CMAKE_CURRENT_SOURCE_DIR}/sources/main.cpp
#)

# define more include directories here
target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/headers
    ${CMAKE_CURRENT_SOURCE_DIR}/third_party
)

# link libraries (3rd party, or like BOOST, or your own added by add_library) here
#target_link_libraries(
#    ${PROJECT_NAME} 
#    PUBLIC
#    lib_name
#)
