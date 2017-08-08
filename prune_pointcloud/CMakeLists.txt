cmake_minimum_required(VERSION 2.8.3)
project(prune_pointcloud)

add_definitions(-std=c++11)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

############
# BINARIES #
############
cs_add_executable(prune_node src/prune_node.cc
                             src/prune.cc)


##########
# EXPORT #
##########
cs_install()
cs_export()
