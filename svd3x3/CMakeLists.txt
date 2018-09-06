cmake_minimum_required(VERSION 3.8)

project(svd3x3)

include_directories(svd3x3
	"./svd3x3"
	"C:/SDKs/cuda/v9.2/Toolkit/include"
	"C:/SDKs/cuda/v9.2/Samples/common/inc"
	)
link_directories("C:/SDKs/cuda/v9.2/Toolkit/lib/x64")

find_package(cuda REQUIRED)
cuda_add_executable(svd3x3
	svd3x3/kernel.cu)
target_link_libraries(svd3x3
	cudart
	cudadevrt
	)