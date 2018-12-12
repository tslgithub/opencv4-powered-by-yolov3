cmake_minimum_required(VERSION 3.8)
project(test) #//项目名称
set(CMAKE_CXX_STANDARD 11)  #//c++版本
include_directories(/home/xxy/opencv4/opencv/build/lib/include)
include_directories(/home/xxy/opencv4/opencv/build/lib/opencv)
include_directories(/home/xxy/opencv4/opencv/build/lib/opencv2)#//opencv引用头文件
#include_directories(/home/xxy/opencv3.2.0/opencv/build/lib/include)
#include_directories(/home/xxy/opencv3.2.0/opencv/build/lib/opencv)
#include_directories(/home/xxy/opencv3.2.0/opencv/build/lib/opencv2)#//opencv引用头文件
set(SOURCE_FILES main.cpp)
set (OpenCV_DIR /home/xxy/openCV/out) #//opnecv头文件库目录
find_package(OpenCV REQUIRED)
add_executable(test ${SOURCE_FILES})
target_link_libraries(test ${OpenCV_LIBS})