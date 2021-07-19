# turtlebot_sim_noetic

Thit is a package allowing to compile and use [turtlebot_simulator](https://github.com/turtlebot/turtlebot_simulator) with ROS noetic.
Currentrly, installing dependencies for this package by using 
```shell
rosdep -i install turtlebot_gazebo
```
does not work, so the dependencies have to be installed manually and compiled together with the package.

## prerquisites

```shell
sudo apt install ros-noetic-kobuki-msgs ros-noetic-kobuki-dock-drive ros-noetic-kobuki-core ros-noetic-ecl-lite ros-noetic-ecl-tools ros-noetic-ecl-core ros-noetic-sophus ros-noetic-robot-pose-ekf python-is-python3 pyqt5-dev-tools
```

## compile and run

To compile the packages contained in this repo

```shell
mkdir -p ~/catkin_ws/src/
cd catkin_ws/
catkin init
cd src/
git clone https://github.com/fvillml/turtlebot_sim_noetic.git
cd ../
catkin build
source devel/setup.bash
```

to run [this](main/launch/turtlebot_sim.launch) launch file
```shell
roslaunch main turtlebot_sim.launch
```