# Turtlebot3_with_SLAM
## task 2
- Frist step: Install TurtleBot3 Packages:
```
sudo apt-get install ros-melodic-dynamixel-sdk
sudo apt-get install ros-melodic-turtlebot3-msgs
sudo apt-get install ros-melodic-turtlebot3 
```
- Second step: install Simulation packages:
```
cd ~/catkin_ws/src/
git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
cd ~/catkin_ws && catkin_make
```
- Third step: write the code:<br/>
<br/>`source ~/catkin_ws/devel/setup.bash`
- Fourth step: open a new terminal from file, now you are ready to launch Simulation World by typing this code:
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_world.launch 
```
-
 ![turtle1-1](https://user-images.githubusercontent.com/85634146/129965272-74c62fe7-a36b-408c-9a24-79596cad0879.png)
 
- Sixth step: open a new terminal from file. Control the robot movement by typing this code:
```
export TURTLEBOT3_MODEL=burger

roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
-
- ![Turtle 2](https://user-images.githubusercontent.com/85634146/129964208-2327f185-1e57-400f-9d36-21d8d7100a4c.jpeg)

- Seventh step: Launch the SLAM Node: in a new terminal tal. run this code:
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping 
```
- 
![turtle3](https://user-images.githubusercontent.com/85634146/129965121-6569f637-2aac-4499-a8a0-00d866cd26a9.jpeg)

-  Final  step: save the map:<br/>
<br/> `rosrun map_server map_saver -f ~/map`
