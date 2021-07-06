# ROS_install_Task1
## ROS Melodic system installation - task 1 for track AI at Smart-Methods summer training

1. Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. Download [Ubuntu 18.04 desktop image](https://releases.ubuntu.com/18.04/) 
**or** [Ubuntu mate 18.04](https://ubuntu-mate.org/download/amd64/bionic/) 

3. create the virtual machine
see the [ubuntu system requirements](https://help.ubuntu.com/community/Installation/SystemRequirements)
[ubuntu mate system requirements](https://ubuntu-mate.org/about/requirements)
![ubuntu VM](VM.PNG)
 **Install ROS melodic**
4. Configure your [Ubuntu repositories](https://help.ubuntu.com/community/Repositories/Ubuntu) <br />
5. Setup your sources.list <br />
Setup your computer to accept software from packages.ros.org. <br />
`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'` <br />
6. Set up your keys <br />
`sudo apt install curl # if you haven't already installed curl` <br />
`curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -` <br />
7. Installation <br />
First, make sure your Debian package index is up-to-date: <br />
`sudo apt update` <br />
- Desktop-Full Install: (Recommended) : ROS, rqt, rviz, robot-generic libraries, 2D/3D simulators and 2D/3D perception <br />
`sudo apt install ros-melodic-desktop-full` <br />
- Desktop Install: ROS, rqt, rviz, and robot-generic libraries <br />
`sudo apt install ros-melodic-desktop` <br />
- ROS-Base: (Bare Bones) ROS package, build, and communication libraries. No GUI tools. <br />
`sudo apt install ros-melodic-ros-base` <br />
8. Environment setup <br />
It's convenient if the ROS environment variables are automatically added to your bash session every time a new shell is launched: <br />
`echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc` <br />
`source ~/.bashrc` <br />
9. Dependencies for building packages <br />
`sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential` <br />
10. Initialize rosdep <br />
`sudo apt install python-rosdep` <br />
`sudo rosdep init` <br />
`rosdep update` <br />
