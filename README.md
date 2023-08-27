# Robot.ST
To download Ros on Ubuntu on Linux:

$sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'


$sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

$sudo apt-get update

$sudo apt-get install ros-kinetic-desktop-full

$apt-cache search ros-kinetic

$echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
$source ~/.bashrc

$sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

$sudo apt install python-rosdep

$sudo rosdep init

$rosdep update

$sudo apt-get install ros-noetic-catkin

$mkdir -p ~/catkin_ws/src

$cd ~/catkin_ws/

$catkin_make

$cd ~/catkin_ws/src

$git clone https://github.com/smart-methods/arduino_robot_arm.git 

$cd ~/catkin_ws

After downloading ros ,Run these commands :

$rosdep install --from-paths src --ignore-src -r -y

packages for for kinetic distro :

$sudo apt-get install ros-kinetic-moveit

$sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

$sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

$sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

Then run these for bash file , you can go to this file via Files - catkin_ws - devel - setup.bash

$sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line
(source /home/hananalganas/catkin_ws/devel/setup.bash)
$source ~/.bashrc

$roslaunch robot_arm_pkg check_motors.launch
then 
ctrl + o

To run TurtleBot on the emulator:

Install Simulation Package :

$ cd ~/catkin_ws/src/
$ git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make

TurtleBot3 World:

$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch


