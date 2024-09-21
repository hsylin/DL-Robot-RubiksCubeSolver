# A Rubik's Cube Solution Using Deep Learning and Robotic Arm Coordination

With the rapid advancement of human-robot collaboration, we can now employ robotic arms for more human-centered tasks. Our goal is to help individuals solve a Rubik's Cube using robotic arms, image recognition, and specialized algorithms.

***
## **Introduction**

We are developing a Rubik's Cube collaboration system that integrates various software and         hardware technologies to achieve human-robot interaction for solving the cube.

- Sensors: RGB-D Depth Camera Realsense D435
- Robotic Arm: TM Robot
- Image Processing: OpenCV
- Algorithm: Kociemba's two-phase algorithm
- Deep Learning: PointNetGPD

## Prerequisite

* Python 3.8.10
* Our requirements in requirements.txt

## Environment

* Ubuntu 20.04.6 LTS
* Intel® Core™ i7-10750H CPU @ 2.60GHz × 12
* NV166 / Mesa Intel® UHD Graphics (CML GT2) 
* Intel® RealSense™ Depth Camera D435

## Training the Model

Please refer to the following format:
[PointCloud_GraspModel](https://github.com/hsylin/PointCloud_GraspModel)

## Usage

**Note:**  
We are currently working to ensure that points 1-5 can be executed independently, which will make testing more convenient and allow for easier integration of new features.

1.Start the hand-eye calibration process to align the coordinates between the camera and the robotics arm.

[TM_RobotArm_Calibration](https://github.com/hsylin/TM_RobotArm_Calibration)
2.Connect the TM robotic arm and import the relevant arm operation functions.

[TM_RobotArm_Control](https://github.com/hsylin/TM_RobotArm_Control)
3.Power on the RealSense D435 and process the input into point cloud data. 

[RealSense](https://github.com/hsylin/RealSense)
4.Receive point cloud data and input it into the trained model, then send the predicted grasping position and orientation to the TM robotic arm for grabbing. 

[TM_RobotArm_Go_Grasp](https://github.com/hsylin/TM_RobotArm_Go_Grasp)
5.Launch the UI to perform the Rubik's Cube solving steps and visualize relevant information about the cube.

[Rubiks_Cube_UI](https://github.com/hsylin/Rubiks_Cube_UI)
## Project Slide
[Slide](https://github.com/hsylin/DL_Robot_RubiksCubeSolver/blob/main/slide.pptx)
## Project Poster
[Poster](https://github.com/hsylin/DL_Robot_RubiksCubeSolver/blob/main/poster.pptx)
## Demo Video

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/aG4lePK26F8/0.jpg)](https://www.youtube.com/watch?v=aG4lePK26F8)
