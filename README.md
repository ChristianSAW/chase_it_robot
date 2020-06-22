# chase_it_robot
Robot that chases a ball in Gazebo (ROS, C++, RViz)

## Getting Setup: 
1. Project will only run on Linux and requires Gazebo + ROS 
2. Click here for Gazebo Download Instructions
3. Click here for ROS Download Instructions

With Gazebo and Ros Installed, you can clone the repository to create your catkin workspace. 

```
$ git clone https://github.com/ChristianSAW/chase_it_robot.git
```

Next, you will need to finish setting up your catkin workspace.

```
$ cd chase_it_robot/catkin_ws/src
$ catkin_init_workspace
```

You are now good to go. To run the existing code, you need to build the exicutables. Use catkin_make to do so.

```
$ cd chase_it_robot/catkin_ws
$ catkin_make
```

Now, to actually lauch gazebo and spawn our robot in the created world, we navigate to the top level catkin workspace, source our setup file, and then run roslaunch as shown below:

``` 
$ cd chase_it_robot/catkin_ws
$ source devel/setup.bash
$ roslaunch my_robot my_robot world.launch
```

To make the robot chase the white ball, open up a new terminal, navigate to the top level catkin workspae, and execute, 

```
$ source sevel/setup.bash
$ roslaunch ball_chaser ball_chaser.launch
```

This will launch the node that processes and image from the forward-facing camera of the robot and commands the robot to chase teh white ball in its field of view.