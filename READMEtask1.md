# TASK1

## Steps to downlaod ROS

1- Downlaod VMware work station 16.

2- Download Ubuntu version 20.04.4

3- Open the Virtual box and press new to create virtual system choose Ubuntu-64bit and change the memory size to 10g

if you are using HP device you maight be facing the error code is 0x80004005 need to change the BIOS setting ( Virtualization Technology (ENable))

4- Restart the system

## **5-WRITE THE instruction Below**

`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`

`sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654`

`sudo apt-get update`

`sudo apt-get install ros-kinetic-desktop-full`

`apt-cache search ros-kinetic`

`echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc source ~/.bashrc`

`sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential`

`sudo apt install python-rosdep`

`sudo rosdep init`

`rosdep update`

![](https://i.postimg.cc/BbXDTdqX/Screenshot-from-2022-08-09-08-30-07.png)
