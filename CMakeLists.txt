cmake_minimum_required(VERSION 3.0.2)
project(custom_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  roscpp
  rospy
  std_msgs
)

add_message_files(
  FILES
  carplace.msg
  xyz.msg
)
generate_messages(
  DEPENDENCIES
  std_msgs
)


catkin_package(
 CATKIN_DEPENDS message_runtime roscpp rospy std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)