cmake_minimum_required(VERSION 2.8)

set(PROJECT_NAME PointerList) 
project(${PROJECT_NAME})
 
set(ExceptionLib ExceptionLib)
set(List List)
set(ListLib ListLib)
set(ListTest ListTest)


set(CMAKE_CONFIGURATION_TYPES "Debug;Release" CACHE STRING "Configs" FORCE)
if(NOT CMAKE_BUILD_TYPE) 
 set(CMAKE_BUILD_TYPE Release) 
endif()

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/ExceptionLib)
add_subdirectory(ExceptionLib)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/ListLib)
add_subdirectory(List)
add_subdirectory(ListLib)
add_subdirectory(ListTest)
add_subdirectory(gtest)
