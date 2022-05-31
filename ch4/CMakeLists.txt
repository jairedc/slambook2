cmake_minimum_required(VERSION 3.0)
project(useSophus)

# To use sophus, it needs to be found using the find_package command
find_package(Sophus REQUIRED)

#Eigen
include_directories("/usr/include/eigen3")
add_executable(useSophus useSophus.cpp)
target_link_libraries(useSophus Sophus::Sophus)

add_subdirectory(example)