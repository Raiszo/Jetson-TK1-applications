cmake_minimum_required (VERSION 2.8)

project(001)

find_package(OpenCV REQUIRED)
find_package(CUDA QUIET REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS} ~/NVIDIA_CUDA-6.5_Samples/common/inc)

cuda_add_executable(001 L1_InverseColors.cu)

target_link_libraries(001  ${OpenCV_LIBS})
