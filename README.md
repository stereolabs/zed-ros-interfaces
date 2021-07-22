![](./images/Picto+STEREOLABS_Black.jpg)

# Stereolabs ZED Camera - ROS Interface

The `zed_interfaces` package defines the custom topics, services and actions used by the [ZED ROS Wrapper](https://github.com/stereolabs/zed-ros-wrapper) to interface with ROS.

If you installed the [ZED ROS Wrapper](https://github.com/stereolabs/zed-ros-wrapper) on the machine it is not required to install also this package because it is automatically integrated by `zed-ros-wrapper` as a git submodule to satisfy all the required dependencies.

You must instead install this package on a remote system that must retrieve the topics sent by the ZED Wrapper (e.g. oject detected by the Object Detection module) or call services and actions to control the ZED.

**Note:** this package does not require CUDA, hence it can be used to receive ZED data also on machines not provided with an Nvidia GPU.

### Prerequisites

- Ubuntu 20.04
- [ZED SDK **≥ 3.5**](https://www.stereolabs.com/developers/) and its dependency [CUDA](https://developer.nvidia.com/cuda-downloads)
- [ROS Noetic](http://wiki.ros.org/noetic/Installation/Ubuntu)

or

- Ubuntu 18.04
- [ZED SDK **≥ 3.5**](https://www.stereolabs.com/developers/) and its dependency [CUDA](https://developer.nvidia.com/cuda-downloads)
- [ROS Melodic](http://wiki.ros.org/melodic/Installation/Ubuntu)

### Build the repository

The `zed_interfaces` is a catkin package. It depends on the following ROS packages:


The zed_ros_wrapper is a catkin package. It depends on the following ROS packages:

- catkin
- std_msgs
- sensor_msgs
- actionlib_msgs
- geometry_msgs
- message_generation

Open a terminal, clone the repository, update the dependencies and build the packages:

$ cd ~/catkin_ws/src
$ git clone https://github.com/stereolabs/zed-ros-interfaces.git
$ cd ../
$ rosdep install --from-paths src --ignore-src -r -y
$ catkin_make -DCMAKE_BUILD_TYPE=Release
$ source ./devel/setup.bash

