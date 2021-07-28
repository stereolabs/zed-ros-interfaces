LATEST CHANGES
==============

2021-07-28
----------
- Added new service `save_memory_map` to save the current area memory to a file to be used in future node running for relocation.

2021-07-27
----------
- Added new service `save_3d_map` to save the current 3D fused point cloud as OBJ or PLY file

2021-07-22
----------
- Created the new repository `zed-ros-interfaces` which contains the ROS package `zed_interfaces` defining the custom topics, services and actions used by the `zed-ros-wrapper`.
This new package is useful to receive the topics from a ZED node on system where the `zed-ros-wrapper` package is not installed, e.g systems without CUDA support.
