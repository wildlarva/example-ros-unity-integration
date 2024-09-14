# Example project for ROS-Unity Joint Control Integration

This is an example project to demonstrate ros-unity-joint-control-integration script.
You can move Panda arm robot on Unity with MoveIt 2 with this example.

## Requirements

- ROS version: ROS 2 humble
- Unity version: 2022.3.46 or above

## How to setup this demo

1. Build demo sources
   1. Unity Side
      1. Clone this demo repository
         ```bash
         git clone --recurse-submodules https://github.com/wildlarva/example-ros-unity-integration.git
         ```
      1. Import cloned project to Unity
      1. Load EmptyScene from Assets/Scenes/EmptyScene.unity
      1. Build the project
   1. ROS Side
      1. Clone panda moveit config for Unity
         ```bash
         git clone https://github.com/wildlarva/moveit_resources.git
         ```
      1. Build the cloned ROS packages with colcon  

1. Setup Unity ROS2 environment.
   * Follow the instruction below:
     * https://github.com/Unity-Technologies/Unity-Robotics-Hub/blob/main/tutorials/ros_unity_integration/setup.md#-ros2-environment

1. Run demo
   1. Unity Side
      1. Run Unity simulation
   1. ROS Side
      1. Launch panda moveit package with Unity option
         ```bash
         ros2 launch moveit_resources_panda_moveit_config demo.launch.py ros2_control_hardware_type:="unity"
         ```
