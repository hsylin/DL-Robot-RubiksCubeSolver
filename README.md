# A Rubik's Cube Solution Using Deep Learning and Robotic Arm Coordination

## **Introduction**

We are developing a Rubik's Cube collaboration system that integrates various software and hardware technologies to achieve human-robot interaction for solving the cube.

- Sensors: RGB-D Depth Camera Realsense D435
- Robotic Arm: TM Robotic Arm TM12M
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

Please refer to this repository for detailed steps on model training:
[PointCloud-GraspModel](https://github.com/hsylin/PointCloud-GraspModel)

## Usage

**Note:**  
We are currently working to ensure that points 1-5 can be executed independently, which will make testing more convenient and allow for easier integration of new features.

1.Connect the TM robotic arm and import the relevant arm operation functions.

[TM-RobotArm-Control](https://github.com/hsylin/TM-RobotArm-Control)

2.Power on the RealSense D435 and process the input into point cloud data. 

[RealSense](https://github.com/hsylin/RealSense)

3.Start the hand-eye calibration process to align the coordinates between the camera and the robotics arm.

[TM-RobotArm-Calibration](https://github.com/hsylin/TM-RobotArm-Calibration)

4.Receive point cloud data and input it into the trained model, then send the predicted grasping position and orientation to the TM robotic arm for grabbing. 

[TM-RobotArm-Go-Grasp](https://github.com/hsylin/TM-RobotArm-Go-Grasp)

5.Launch the UI to display the Rubik's Cube solving process and visualize relevant information about the cube.

[Rubiks-Cube-UI](https://github.com/hsylin/Rubiks-Cube-UI)

## Project Report
[Report](https://github.com/hsylin/DL-Robot-RubiksCubeSolver/blob/main/report.pdf)
## Project Poster
[Poster](https://github.com/hsylin/DL-Robot-RubiksCubeSolver/blob/main/poster.pdf)
## Demo Video

**Note:** The demo video has been sped up due to the slow movement speed of the robotic arm.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/aG4lePK26F8/0.jpg)](https://www.youtube.com/watch?v=aG4lePK26F8)

## Future Work

- **Exploration of LLM as High-Level Planners**: Although the use of large language models (LLMs) as high-level planners may offer limited advantages for tasks with fixed processes, such as solving the Rubik's Cube, We intend to explore this approach as a valuable learning opportunity. By enabling LLMs to manage and coordinate multiple low-level APIs, We can explore their potential for open-vocabulary task planning in more complex robotic systems.
  
- **API Modularization**: We plan to modularize key components—including PointNetGPD for grasping pose estimation, robotic arm control, gripper manipulation, and Kociemba’s two-phase algorithm—into distinct APIs. This modular design will allow for seamless integration with the LLM-based planner, improving system flexibility, scalability, and reusability across a wider range of robotic applications.
  
- **Lighting Adjustment API**: To enhance visual processing robustness under varying environmental conditions, We propose the development of a lighting adjustment API. This API will dynamically adjust camera parameters to ensure optimal system performance and maintain reliability across different lighting scenarios.


## Reference

[Kociemba's two-phase algorithm](https://github.com/hkociemba/RubiksCube-TwophaseSolver)

[PointNet](https://github.com/charlesq34/pointnet)

[PointNetGPD](https://github.com/lianghongzhuo/PointNetGPD)





