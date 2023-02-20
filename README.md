# Assignment2

## Tasks achived
- A URDF robot was created with a laser and a manipulator, which consists of three revolute joints and one prismatic joint. A camera is attached to the tip of the manipulator to scan the  aruco markers, as illustrated in the figures below. 
![image](https://user-images.githubusercontent.com/73067092/219985696-f6def257-d659-403b-96f9-8922f3666b45.png)
![image](https://user-images.githubusercontent.com/73067092/219985786-7fd01baf-8498-4479-8d21-4ff81efd508f.png)
- The images above indicate that the robot has been successfully spawned in both RVIZ and Gazebo, positioned at x = -6.0 and y = 11.0 in the environment.
- Configuring the PID parameters is a crucial step in ensuring the stability of the robot arm. 
- Once the arm is stable, I am able to precisely control each joint of the arm to scan markers using a camera and the aruco_ros package.
-  I can control the robot's movement using the topic cmd_vel publisher, which can be accessed through the "rosrun rqt_robot_steering rqt_robot_steering" command.

## Tasks need to accomplish:
- The scanning of aruco markers currently requires manual control of the arm joints, but the goal is to automate this process through code. The angles required to locate each marker are known and can be found in the "robot_state_machine.py" file under the "scan_environment" function
- Additionally, the attempt to survey rooms using the ontology failed when the robot's battery became low. To recharge, the robot needs to reach room E, but it encountered errors when trying to locate some necessary files, as indicated below.
![image](https://user-images.githubusercontent.com/73067092/219987907-185e2d2f-ea7b-443e-b645-ec1879216043.png)

### Installation

Follow these steps to install the software.
 - Clone this repository inside your ROS workspace (which should be sourced in your `.bashrc`).
 ```bash
$ cd <your ROS ws/src>
$ git clone https://github.com/Vallamkondavishal/Expo_Robotics_Assignment-2.git
$ cd ..
$ catkin_make
```
 
 - Run `chmod +x <file_name>` for each file inside the `scripts` folder.
 - Run `catkin_make` from the root of your ROS workspace.
 - Install `xterm` by entering the command `sudo apt install -y xterm`.

### Launchers

Use the following command to launch the software with randomized stimulus.
```bash
roslaunch assignment2 assignment.launch  

```




