# Catkin User Guide: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/user_guide.html
# Catkin CMake Standard: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/standards.html
cmake_minimum_required(VERSION 2.8.3)
project(calvin_pick_n_place)
# Load catkin and all dependencies required for this package
# TODO: remove all from COMPONENTS that are not catkin packages.
find_package(catkin REQUIRED COMPONENTS roscpp tf actionlib moveit_ros_planning_interface control_msgs geometry_msgs moveit_msgs object_recognition_msgs shape_msgs visualization_msgs)

# catkin_package parameters: http://ros.org/doc/groovy/api/catkin/html/dev_guide/generated_cmake_api.html#catkin-package
catkin_package(
    CATKIN_DEPENDS roscpp tf actionlib moveit_ros_planning_interface control_msgs geometry_msgs moveit_msgs object_recognition_msgs shape_msgs visualization_msgs
)

include_directories(${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS})

add_executable(calvin_pick_n_place src/calvin_pick_n_place.cpp)


