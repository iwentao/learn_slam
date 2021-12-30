#set(CMAKE_C_FLAGS "-g -Wall  -I C:\\TDM-GCC-32\\include -L C:\\TDM-GCC-32\\lib")
set(CMAKE_C_FLAGS "-g -Wall  -I C:\\TDM-GCC-64\\include -L C:\\TDM-GCC-64\\lib")
set(CMAKE_CXX_COMPILER "g++")
set(CMAKE_CXX_FLAGS "-g -Wall  -I C:\\TDM-GCC-64\\include -L C:\\TDM-GCC-64\\lib") 
include_directories("../3rdParty/eigen-3.4.0")

project(EigenTest)
SET(SRC_LIST eigenMatrix.cpp)

add_executable(eigenTest ${SRC_LIST})