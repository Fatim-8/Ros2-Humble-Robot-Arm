# Ros2-Humble-Robot-Arm

This project provides guidance on launching an URDF model for a robot arm using STL files in the ROS2 Humble environment. The project includes["the robot-arm-pkg package"](https://github.com/smart-methods/arduino_robot_arm/tree/main/robot_arm_pkg), which contains the URDF model, and was created by[Smart-Methods](https://github.com/smart-methods).

# Overview

This package enables users to view and manipulate a robot arm model in the ROS2 Humble environment using RViz and MoveIt2. It includes the necessary URDF and STL files to represent the robot arm.

 [moveit_pkg](https://github.com/smart-methods/arduino_robot_arm/tree/main/moveit_pkg)

 [robot_arm_pkg](https://github.com/smart-methods/arduino_robot_arm/tree/main/robot_arm_pkg)

# Installation

1. Create the Workspace
```
mkdir -p ~/robot_arm_ros2_ws/src
```
```
cd ~/robot_arm_ros2_ws/src
```
2. Download the package
```
git clone https://github.com/MoAlharsani/ros2-humble-robot-arm.git
```
```
mv ros2-humble-robot-arm/robot_arm_description ros2-humble-robot-arm/moveit_pkg 
```
```
rm -rf ros2-humble-robot-arm
```
3. Build, source, and launch the package.
```
cd ~/robot_arm_ros2_ws/
```
```
colcon build
```
```
source ~/robot_arm_ros2_ws/install/setup.bash
```
3.1 To run the URDF Model In RViz.
```
ros2 launch robot_arm_description display.launch.py
```

3.2 To run the URDF Model In RViz with MoveIt Plugin
```
ros2 launch moveit_pkg demo.launch.py
```
