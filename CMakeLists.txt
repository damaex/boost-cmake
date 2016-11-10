cmake_minimum_required(VERSION 2.8)
project(BoostTest)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)

set(Boost_USE_STATIC_LIBS ON)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME ON)

find_package(Boost 1.46.0 COMPONENTS filesystem)

if(Boost_FOUND)
    include_directories(${Boost_INCLUDE_DIRS})
    add_executable(BoostTest ${SOURCE_FILES})
    target_link_libraries(BoostTest ${Boost_LIBRARIES})
else(Boost_FOUND)
    message(FATAL_ERROR "Boost not found.")
endif(Boost_FOUND)