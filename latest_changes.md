LATEST CHANGES
==============

2021-07-22
----------
- Created the new repository `zed-ros-interfaces` which contains the ROS package `zed_interfaces` defining the custom topics, services and actions used by the `zed-ros-wrapper`.
This new package is useful to receive the topics from a ZED node on system where the `zed-ros-wrapper` package is not installed, e.g systems without CUDA support.
