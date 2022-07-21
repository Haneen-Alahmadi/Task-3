# Task-3
After installing ROS1
Install the package Arduino robot arm

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

sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line
(source /home/wesam/catkin_ws/devel/setup.bash)
then 
ctrl + o

source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch
#After install "roslaunch robot_arm_pkg check_motors.launch" (RVIZ) will appear
<img width="942" alt="Screen Shot 1443-12-22 at 5 59 27 AM" src="https://user-images.githubusercontent.com/108179353/180120900-d98a0403-6aba-448b-a545-4693c134052b.png">

