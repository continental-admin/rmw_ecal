# eCAL ROS2 middleware layer

ROS2 middleware based on eCAL.

eCAL RMW can offer:

* High performance (shared memory is used for inter-process communication and udp multicast for inter-host communication)
* All eCAL ecosystem tools to
  * monitor all ros publisher / subscriber / services using the [eCAL Monitor](https://continental.github.io/ecal/getting_started/monitor.html)
  * record all ROS messages decentralized into HDF5 without extra network load using the [eCAL Recorder](https://continental.github.io/ecal/getting_started/recorder.html)
  * replay ROS messages using the [eCAL Player](https://continental.github.io/ecal/getting_started/player.html) utility

## Build instructions

### Linux

* Install [eCAL](https://github.com/continental/ecal)
* Clone latest release of this repository into your [ROS2 workspace](https://index.ros.org/doc/ros2/Tutorials/Workspace/Creating-A-Workspace/)
* Source ROS2 `source /path/to/your/ros/distro/folder/setup.bash`
* Run `colcon build` from your workspace folder
* Setup your workspace `source /path/to/your/workspace/install/setup.bash`
* Specify ecal as rmw implementation `export RMW_IMPLEMENTATION=rmw_ecal_dynamic_cpp`

### Windows

* Install [eCAL](https://github.com/continental/ecal)
* Clone latest release of this repository into your [ROS2 workspace](https://index.ros.org/doc/ros2/Tutorials/Workspace/Creating-A-Workspace/)
* Source ROS2 `call C:/path/to/your/ros/distro/folder/setup.bat`
* Run `colcon build` from your workspace folder
* Setup your workspace `call C:/path/to/your/workspace/install/setup.bat`
* Specify ecal as rmw implementation `set RMW_IMPLEMENTATION=rmw_ecal_dynamic_cpp`

### Currently supported ROS2 distributions

* Dashing Diademata
* Eloquent Elusor
* Foxy Fitzroy
