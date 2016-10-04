cmake_minimum_required(VERSION 3.3)

project(boost_ratio)

add_library(boost_ratio INTERFACE)

target_include_directories(boost_ratio BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_ratio DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::ratio ALIAS boost_ratio)
