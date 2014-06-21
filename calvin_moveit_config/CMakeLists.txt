cmake_minimum_required(VERSION 2.8.3)
project(calvin_moveit_config)

find_package(catkin REQUIRED COMPONENTS calvin_description)

catkin_package(
            CATKIN_DEPENDS calvin_description)

install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
