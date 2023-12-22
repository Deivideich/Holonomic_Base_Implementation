Holonomic_Base_Simulation

Simulation in Gazebo for an autonomous holonomic base using ROS 2. The project is designed for compatibility with ROS Foxy, emphasizing the use of ROS 2 tools such as Nav2 for navigation and ROS 2 control for enhanced control applications in holonomic structures.

To run the octobot_2 package, switch to the ROS Foxy distribution using source /opt/ros/foxy/setup.bash, then run source install/setup.bash and colcon build. Note that Python was used for package creation; however, switch to CMake if necessary.

Use the following launch commands:

    ros2 launch octobot_2 display.launch.py to visualize the robot in RVIZ.
    ros2 launch octobot_2 gazebo.launch.py to simulate the robot in Gazebo.
    ros2 launch octobot_2 rsp.launch.py for launching only robot state publisher
    ros2 launch gazebo_ros gazebo.launch to run gazebo
    ros2 run gazebo_ros spawn_entity.py -topic robot_description -entity robot_name to spawn robot in gazebo manually (after using rsp launch file, for example)
    ros2 launch gazebo_ros gazebo.launch to run gazebo
    killall gzserver
    killall gzclient - If gazebo fails
    ros2 run teleop_twist_keyboard teleop_twist_keyboard to run teleop (should be compatible after spawning robot in gazebo since lib_gazebo_planar_movement admits cmd_vel as default)
    
    
Compatibility with Xacro commands is still in progress

Feel free to change URDF, but dont forget to include package dependencies in setup.py file

Remember to include the octobot_2 file located outside ros_2_ws within the "models" folder in your Gazebo .gazebo file. This file contains essential meshes for proper visualization.

Important Note:
Ensure that all dependencies are installed, and switch to CMake if required for your specific use case.
