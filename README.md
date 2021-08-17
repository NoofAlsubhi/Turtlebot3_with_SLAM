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
- pic
-
- Sixth step: open a new terminal from file. Control the robot movement by typing this code:
```
export TURTLEBOT3_MODEL=burger

roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
- pic
- Seventh step: Launch the SLAM Node: in a new terminal tal. run this code:
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping 
```
- pic
- Eighth step: save the map:<br/>
<br/> `rosrun map_server map_saver -f ~/map`
- pic
- pic
