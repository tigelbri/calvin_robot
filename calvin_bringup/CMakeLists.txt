# Catkin User Guide: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/user_guide.html
# Catkin CMake Standard: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/standards.html
cmake_minimum_required(VERSION 2.8.3)
project(calvin_bringup)
# Load catkin and all dependencies required for this package
find_package(catkin REQUIRED COMPONENTS calvin_description calvin_joint_commander imu_filter_madgwick katana laser_filters libuvc_camera openni_launch phidgets_imu robot_pose_ekf robot_state_publisher sick_tim3xx volksbot_driver)

#include_directories(include ${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS})

catkin_package(
    CATKIN_DEPENDS calvin_description calvin_joint_commander imu_filter_madgwick katana laser_filters libuvc_camera openni_launch phidgets_imu robot_pose_ekf robot_state_publisher sick_tim3xx volksbot_driver
)
