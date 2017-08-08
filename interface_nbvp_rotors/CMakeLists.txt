cmake_minimum_required(VERSION 2.8.3)
project(interface_nbvp_rotors)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

############
# BINARIES #
############

cs_add_executable(exploration src/exploration.cpp)

##########
# EXPORT #
##########
cs_install()
cs_export()
