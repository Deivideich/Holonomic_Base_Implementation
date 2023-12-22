# Holonomic_Base_Simulation
Simulation in Gazebo for an autonomous holonomic base using ROS2
The first stage of development has been developed in order to be compatible with ROS Noetic and ROS Foxy, but will change in order to be fully compatible with most of ROS2 tools, such as Nav2 instead of navstack and ROS2_control if possible for better control application in holonomic structures

In oder to run/use the octobot_2 package, it is mandatoy to change to ROS foxy distro, and use source /opt/ros/foxy/setup.bash, and source install/setup.bash and colcon build instead of catkin_make

Also, the package is designed in order to run ros2 launch octobot_2 display.launch.py or gazebo.launch.py or rsp.launch.py in order to simulate or see the robot in RVIZ

Dont forget to include the octobot_2 file that is outside ros_2_ws which only contains meshes in your .gazebo inside the folder "models", otherwise, nothing will be shown

Important note: instead of using Cmake in order to run the packages python was used running: ros2 pkg create --build-type ament_python <package_name>, dont forget to change to cmake instead if necessary
