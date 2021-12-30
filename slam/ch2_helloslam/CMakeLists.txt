set(CMAKE_C_FLAGS "-g -Wall  -I C:\\TDM-GCC-32\\include -L C:\\TDM-GCC-32\\lib")
set(CMAKE_CXX_COMPILER "g++")
set(CMAKE_CXX_FLAGS "-g -Wall  -I C:\\TDM-GCC-32\\include -L C:\\TDM-GCC-32\\lib") 

project(HelloSLAM)
SET(SRC_LIST helloSLAM.cpp)

add_executable(helloSLAM ${SRC_LIST})
add_library(hello libHelloSLAM.cpp)
add_library(hello_shared SHARED libHelloSLAM.cpp)

add_executable(useHello useHello.cpp)
target_link_libraries(useHello hello_shared)