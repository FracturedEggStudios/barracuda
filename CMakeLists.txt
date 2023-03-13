cmake_minimum_required(VERSION 3.22)
project(barracuda CUDA)

#if(NOT DEFINED ${CMAKE_CUDA_ARCHITECTURES})
#    set(CMAKE_CUDA_ARCHITECTURES 52 61 75)
#endif()
message(STATUS "CUDA architectures set to ${CMAKE_CUDA_ARCHITECTURES}")
#

set(CMAKE_CUDA_STANDARD 17)

add_executable(barracuda main.cu)

set_target_properties(barracuda PROPERTIES
        CUDA_SEPARABLE_COMPILATION ON)
