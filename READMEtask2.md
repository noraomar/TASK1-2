# TASK2
Ros on Jetson Nano

1- Download xubuntu 20.04 on jetson nano

https://github.com/Discombobulated88/Xubuntu-20.04-L4T-32.3.1/releases/download/v1.0/Xubuntu-20.04-l4t-r32.3.1.tar.tbz2

2- Download balena

https://www.balena.io/etcher/


5- Flash from memory then upload the image file  xubuntu > Select target sd card > Then press flash

8-  connect the sd car into ubuntu

9- open boot folder > extlinux  >in the terminal write this instructions `cd` > `ls` 10- copy file name b00.dtb and then write those instruction

`cd extlinux`

`sudo gedit extlinux.conf open extlinux.conf `> write FDT/BOOT and paste dtb file name

11- Eject SD card from Ubuntu system

12- insert sd on jetson nano > Boot on jetson nano > install and reboot

13- open terminal then write the  instruction

**Set locale**


`locale # check for UTF-8`

`sudo apt update && sudo apt install locales`

`sudo locale-gen en_US en_US.UTF-8`

`sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8`

`export LANG=en_US.UTF-8`

`locale # verify settings`

set up source

`apt-cache policy | grep universe`



`500 http://us.archive.ubuntu.com/ubuntu focal/universe amd64 Packages release v=20.04,o=Ubuntu,a=focal,n=focal,l=Ubuntu,c=universe,b=amd64`


 add the ROS 2 apt repository the system

`sudo apt update && sudo apt install curl gnupg2 lsb-release sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg`

 add the repository to the  sources list.

`echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null`

**Install ROS 2 packages**

Update  apt repository caches 

`sudo apt update`

**ROS 2 packages are built on frequently updated Ubuntu systems its better to upgrade**

`sudo apt upgrade`

**Desktop Install**

`sudo apt install ros-foxy-desktop`

ROS-Base Install (Bare Bones): Communication libraries, message packages, command line tools. No GUI tools.

`sudo apt install ros-foxy-ros-base`

**Environment setup**

`echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc source ~/.bashrc`
