UR5e Gazebo Simulation and 3D Reconstruction

This repository provides a Gazebo simulation for the UR5e robot with a 4-finger custom gripper and an associated 3D reconstruction module.
Requirements

    ROS (tested on [your ROS distribution, e.g., Kinetic/Noetic])
    Gazebo
    MoveIt!
    [Other dependencies your project may need]

Setup

    Clone this repository into your catkin workspace (/catkin_ws/src).
    Build your workspace:

    cd /catkin_ws
    catkin_make
    source devel/setup.bash

Running the Simulation
Start ROS Core

In a terminal, run:

roscore

Launch the Gazebo Simulation

In another terminal, launch the UR5e simulation with the custom gripper:

roslaunch ur5e_gazebo_sim ur5e_4_finger_custom_gripper.launch

Run the Gripper Movement Script

Once Gazebo is up and running, execute the script to move the gripper towards the box:

rosrun ur5e_gazebo_sim ur5e_4_finger_gripper_move_to_box.py

Running the 3D Reconstruction

To perform 3D reconstruction using structure-from-motion (SfM), run the following command:

rosrun ur5e_gazebo_sim sfm.py

Dataset Information

The dataset required for 3D reconstruction is located in:

/catkin_ws/src/sift_ros/dataset

This folder contains:

    Calibration images and videos
    Item images and videos

Ensure that the dataset is correctly placed in the specified directory before running the 3D reconstruction module.
Notes

    Make sure all required packages and dependencies are installed.
    Adjust file paths and parameters as needed to suit your configuration.
    For any issues or additional configuration details, please refer to the project's documentation or contact the maintainer.
