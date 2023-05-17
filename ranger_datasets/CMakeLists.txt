cmake_minimum_required(VERSION 3.0.2)
project(ranger_datasets)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp std_msgs nav_msgs tf)

## Declare a catkin package
catkin_package()

## Specify additional locations of header files
include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(republisher_odom_tf src/republisher_odom_tf.cpp)
target_link_libraries(republisher_odom_tf ${catkin_LIBRARIES})
