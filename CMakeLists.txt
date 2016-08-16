#Generate only regex library only for centos
cmake_minimum_required(VERSION 2.8)

file(GLOB REGEX_SOURCES  libs/regex/src/*.cpp)

include_directories(./)

add_library(boost_regex STATIC ${REGEX_SOURCES})

