cmake_minimum_required(VERSION 2.8.3)
project(multiagent_collision_check)

add_definitions(-std=c++11)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

cs_add_library(${PROJECT_NAME} src/multiagent_collision_checker.cpp)

##########
# EXPORT #
##########
cs_install()
cs_export()
