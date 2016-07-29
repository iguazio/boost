#Generate only regex library only for centos
cmake_minimum_required(VERSION 2.8)

if(${CENTOS})

    set(REGEX_SOURCES_PATH ${BOOST_PATH}/libs/regex/src)
    set(REGEX_HEADERS_PATH ${BOOST_PATH}/boost ${BOOST_PATH}/boost/regex)

    file(GLOB REGEX_SOURCES  ${REGEX_SOURCES_PATH}/*.cpp)

    include_directories(${BOOST_PATH})

    add_library(boost_regex STATIC ${REGEX_SOURCES} )
    
endif()

