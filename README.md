# Task3_robot_arm

Task3_robot_arm
Learn how to install and run the arms package on Ros using Ubuntu and how to create a workspace with steps In the previous task, the ros system was installed

Steps:
Open the terminal

Copy the commands

$ sudo apt install ros-noetic-catkin
Used to create a workspace for an arm

Note: The folder can be called by any name

$ mkdir -p ~/catkin_ws/src
Create another folder inside "catkin _ws" with the name 'src'

$ cd ~/catkin_ws/
Go to the folder catkin_ws and download the package

$ catkin_make
Go to the folder src and download the package

$ cd ~/catkin_ws/src
Download the git package for access to the robot arm package

$ sudo apt install git
$ git clone https://github.com/smart-methods/arduino_robot_arm.git
Go to the folder and download the package

$ cd ~/catkin_ws
if Command 'rosdep' is not found, but can be installed with:

$ sudo apt install python3-rosdep2
$ rosdep update
Note the above command can be written before creating the workspace

$ rosdep install --from-paths src --ignore-src -r -y
Download all the packages inside the workspace and run them There are many versions and this package for noetic

$ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
After opening the terminal, open the bashrc file using the command

$ sudo nano ~/.bashrc
At the_end_ of the file add

> source /home/shurooq/catkin_ws/devel/setup.bash
Note: Username varies from person to person

Ctrl+o -> write out

Enter

Ctrl+x -> Exit

  $ source ~/.bashrc
File update

 $ roslaunch robot_arm_pkg ckeck_motors.launch
Rviz will run,The arm movement can be simulated and controlled
