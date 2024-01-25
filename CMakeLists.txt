cmake_minimum_required(VERSION 3.0.2)
project(uwb_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

## Generate messages in the 'msg' folder
add_message_files(
   FILES
   RangeStamped.msg
   PassiveStamped.msg
   CirStamped.msg
   TagsStateStamped.msg
)

add_service_files(
  FILES
  Range.srv
  InitiateTwr.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
)

catkin_package()

include_directories(
    ${catkin_INCLUDE_DIRS}
)