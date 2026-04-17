
# Niryo One Robotic Arm for Dental Tool Manipulation 🤖🦷

## Abstract

This project presents an application of artificial intelligence for the precise manipulation of dental tools using a robotic arm. The system focuses on isolating a specific tool from a set of visually similar metal instruments placed on a workbench.

A vision-based recognition pipeline is used to detect the target tool and estimate its position and orientation for robotic grasping. The approach enables real-time image processing with accurate localization and orientation estimation, supporting reliable robotic manipulation.

---

## Methodology

### Object Detection and Classification

The **YOLO (You Only Look Once)** algorithm is used for tool detection and classification.

- Dataset: 11 classes of dental tools  
- Task: Identify and isolate a specific tool from a cluttered scene  
- Output: Bounding/segmentation information for the selected tool  

The model achieves a detection accuracy of **98.4%** in the image system.

---

### Pose Estimation

Tool pose is computed using geometric processing:

- **Position estimation** is derived from the detected tool location in the image  
- **Orientation estimation** is computed using Principal Component Analysis (PCA) applied on the tool shape  

This allows extraction of the tool rotation on the workbench.

---

### Robotic Manipulation

The estimated pose is mapped into the robot workspace to define the starting point for motion planning.

- Robot: Niryo One robotic arm  
- Motion planning: **RRT-Connect algorithm**  
- Trajectory refinement: interpolation-based error compensation for end-effector stability  

The system achieves a capture precision of approximately **±3 mm**.

---

## Experimental Results

Experiments demonstrate that the system is capable of:

- Successfully detecting and isolating the target tool  
- Estimating position and orientation with high accuracy  
- Executing reliable grasping actions using the robotic arm  
- Completing the manipulation task based on user selection  

---

## Keywords

YOLO, PCA, Deep Learning, Object Detection, Classification, Robotic Manipulation, RRT-Connect

## rqt_graph 
![rqt](https://github.com/kheirbeqaya/Niryo-Arm-as-a-dental-surgeon-assistant/blob/f83bb864ae18e12878a70309206bd25e052ce5cd/rqt.png)

## Acknowledgements 
gratitude to Manara University for allowing us to use their equipment.


## Author
Aya Kheir Beq MSc in Mechatronics Engineering Focus: Computer Vision, Robotics, Intelligent Systems


