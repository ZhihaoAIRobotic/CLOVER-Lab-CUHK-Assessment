# CLOVER-Lab-CUHK-Assessment


Description
-------
Grasping is an important skill in our daily manipulation task. But it is still challenging for robots to perform grasping tasks in the
unstructured environments in the real world. The goal of this task is to predict the quality and pose of
grasps based on vision.   

**Grasp Representation**: Parameterised as a grasp quality, 
angle and gripper width for every pixel in the input image

**Grasp Quality**: Describe the quality of a grasp
executed at each pixel. The value is a scalar in the
range [0, 1] where a value closer to 1 indicates higher grasp
quality, i.e. higher chance of grasp success. 

**Angle**: Describe the angle of a grasp to
be executed at each point. 

**Width**: Describe the gripper width of a grasp
to be executed at each point.

![](images/input_output.png)


Dataset
-------
We use cornell grasp dataset in this task. The dataset can be found here:
https://www.kaggle.com/datasets/oneoneliu/cornell-grasp

>pcd*.txt is point cloud file, pcd*cneg.txt 
> is negative label for grasp, 
> pcd*cpos.txt is positive label for grasp,
>pcd*d.tiff is depth image,
>*.png is raw rgb image.

To generate the ground truth for the network, 
the data process method are as follows:

**Grasp Quality**: Each ground-truth positive grasp from 
the Cornell Grasping Dataset as a binary label and set
the corresponding area of Q_T to a value of 1. All other 
pixels are 0.

**Angle**: Compute the angle of each grasping rectangle
in the range [−π/2,π/2].

**Width**: Compute the width in 
pixels (maximum of 150) of each grasping rectangle.

Evaluation
-------

