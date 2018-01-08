##Stop 2 Senconds
a modification based on lane following demo
##How to Use it?
* get and compile the latest version of duckietown software on your computer
* make the following modifications:
  1. at [duckietown_demos package]/launch/, put in [duckiedev]/launch/lane_following_dev.launch
  2. at [veh_coordination package]/src, replace fake_coordinator_node.py with [duckiedev]/src/fake_coordinator_node.py
* setup your duckietown enviroments and run:
>roslaunch duckietown_demos lane_following_dev.launch
