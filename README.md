graspit_interface
=================

This plugin exposes a ROS interface for the GraspIt! simulator. Our main purpose for writing
this plugin was to give GraspIt! more exposure to the ROS community and make it easier to
get started planning grasps with GraspIt! You can interact with this interface through a
variety of ROS services and action servers.

If you have any specific features you'd like to see, let us know by submitting a new issue, or feel free to submit a pull request!

To see how a client interacts with this interface, check out our python client
[graspit_commander](https://github.com/CURG/graspit_commander).


Setup:
------
```
//create ros workspace
mkdir -p graspit_ros_ws/src
cd graspit_ros_ws/src

source /opt/ros/indigo/setup.bash
catkin_init_workspace . 

//clone packages
git clone https://github.com/graspit-simulator/graspit-ros.git --recursive
git clone https://github.com/CURG/graspit_interface.git
git clone https://github.com/CURG/graspit_commander.git

//build workspace
cd graspit_ros_ws
catkin_make
```


Launching graspit_interface:
-------
```
source devel/setup.bash
roslaunch graspit_interface graspit_interface.launch
```

Then you can view available services and topics provided by the graspit_interface via:
```
rostopic list
rosservice list
```
