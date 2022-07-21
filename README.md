# Task-3 
Install the package Arduino robot arm

After installing ROS1

#Add the (arduino robot arm) package to (src) folder

sudo apt-get install ros-noetic-catkin

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm

#Install all the dependencies

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

#for noetic distro . NOTE "You will get problems when installing packages that don't follow your ROS version"

$ sudo apt-get install ros-noetic-moveit

$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

# change dictionary

cd

sudo nano ~/.bashrc

# at the end of the (bashrc) file add the follwing line

source /home/parallels/catkin_ws/devel/setup.bash

#then enter

ctrl + o

ENTER

ctrl + x

source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch

#After install "roslaunch robot_arm_pkg check_motors.launch" (RVIZ) will appear

<img width="931" alt="image" src="https://user-images.githubusercontent.com/108179353/180121298-9d45bf4d-0d82-4fcc-8749-e4c31f087942.png">
