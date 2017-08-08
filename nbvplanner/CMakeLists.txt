cmake_minimum_required(VERSION 2.8.3)
project(nbvplanner)

add_definitions(-std=c++11)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

#############
# LIBRARIES #
#############

cs_add_library(nbvPlannerLib src/mesh_structure.cpp
                          src/nbvp.cpp
                          src/rrt.cpp
                          src/tree.cpp)

############
# BINARIES #
############

cs_add_executable(nbvPlanner src/nbv_planner_node.cpp
                          src/mesh_structure.cpp
                          src/nbvp.cpp
                          src/rrt.cpp
                          src/tree.cpp)
target_link_libraries(nbvPlanner nbvPlannerLib)

##########
# EXPORT #
##########

cs_install()
cs_export()
