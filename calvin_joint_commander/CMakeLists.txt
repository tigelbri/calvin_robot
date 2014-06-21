# Catkin User Guide: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/user_guide.html
# Catkin CMake Standard: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/standards.html
cmake_minimum_required(VERSION 2.8.3)
project(calvin_joint_commander)
# Load catkin and all dependencies required for this package
find_package(catkin REQUIRED COMPONENTS roscpp dynamic_reconfigure std_msgs sensor_msgs)

include_directories(include ${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS})

#add dynamic reconfigure api
include(${dynamic_reconfigure_PACKAGE_PATH}/cmake/cfgbuild.cmake)
gencfg()

catkin_package(
    CATKIN_DEPENDS roscpp dynamic_reconfigure std_msgs sensor_msgs
)

target_link_libraries(${PROJECT_NAME} ${Boost_LIBRARIES})
add_executable(joint_commander src/joint_commander.cpp)


