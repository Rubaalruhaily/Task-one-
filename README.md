# Task-one-
## Install ROS and Arm Package

 * First of all we will Download ROS on Ubuntu 
 we will use this Codes In Terminal 
 *[ The Codes ]
```
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
$ sudo apt-get update
```


### I downloaded ROS melodic Version 

```
$ sudo apt-get install ros-melodic-desktop-full
$ apt-cache search ros-melodic
$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
```


![01](https://user-images.githubusercontent.com/86341464/123764587-96831380-d8cd-11eb-8e9d-384a0eb52c1f.PNG)

* After Installing ROS Melodic I installed Python Using These Codes 
```
$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
$ sudo apt install python-rosdep
$ sudo rosdep init
$ rosdep update
$ sudo apt-get install ros-melodic-catkin
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
$ cd ~/catkin_ws/src
```


#### Downloding The arm package from S-M Github

```
$ git clone https://github.com/smart-methods/arduino_robot_arm.git 
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-melodic-moveit
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
```
 Then I change The path 

 runing The final code to move and control robot arm 
  using this code and run it 
	
	``` $ roslaunch robot_arm_pkg check_motors.launch ```
 
 ![1](https://user-images.githubusercontent.com/86341464/123764391-6b002900-d8cd-11eb-9b8a-2bc799981ff8.PNG)


