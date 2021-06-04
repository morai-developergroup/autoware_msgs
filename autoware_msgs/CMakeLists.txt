cmake_minimum_required(VERSION 2.8.3)
project(autoware_msgs)


find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

 add_message_files(
   DIRECTORY msg
   FILES
   ControlCommand.msg
   ControlCommandStamped.msg
   VehicleStatus.msg
   Gear.msg
 )

 generate_messages(
   DEPENDENCIES
   std_msgs
 )

catkin_package(
  CATKIN_DEPENDS 
std_msgs 
message_runtime
)

