cmake_minimum_required(VERSION 2.8.3)
project(ras_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs sensor_msgs)

add_message_files(
  DIRECTORY msg
  FILES
    RAS_Evidence.msg
	Shape.msg
	Object_id.msg
	Cam_transform.msg
	pcl_object.msg
	pcl_object_mult.msg
)


generate_messages(
  DEPENDENCIES std_msgs sensor_msgs
)

