Implementation of a 4 omniwheeled robot for @Home competiton

This repository hosts the simulation in ROS 2 (Foxy) and implementation in ROS 1 (Noetic) of a holonomic robot designed to carry a Xarm 6 in order to accomplish different tasks in a house-like environment.

It is designed to use Hector SLAM in order to generate maps, odometry (With scan match, encoder readings and IMU) and be used by Navstack so that the robot can handle waypoints following and obstacle avoidance

Remember to include the octobot_2 file located inside Holonomic_Base_Simulation within the "models" folder in your Gazebo .gazebo file. This file contains essential meshes for proper visualization.
