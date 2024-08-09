mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
cd ~/catkin_ws/src

catkin_create_pkg my_simple_package rospy

cd ~/catkin_ws

catkin_make
chmod +x ~/catkin_ws/src/my_simple_package/src/simple_node.py
cd ~/catkin_ws
catkin_make
source devel/setup.bash
roslaunch my_simple_package simple_launch.launch
