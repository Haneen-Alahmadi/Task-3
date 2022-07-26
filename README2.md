#1- Install arduino ide on ubuntu 20.04

cd arduino

sudo ./install.sh

./arduino

#Install rosserial

sudo apt-get install ros-noetic-rosserial-arduino

sudo apt-get install ros-noetic-rosserial


#2- Install ros_lib into the Arduino Environment
 
 cd Arduino/libraries
 
 rm -rf ros_lib
 
 rosrun rosserial_arduino make_libraries.py .
