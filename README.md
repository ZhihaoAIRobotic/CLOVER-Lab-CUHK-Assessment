# CLOVER-Lab-CUHK-Assessment


##Description
Grasping is an important skill in our daily manipulation task. But it is still challenging for robots to perform grasping tasks in the
unstructured environments in the real world. The goal of this task is to predict the quality and pose of
grasps based on vision.   

**Grasp Representation**: 

**Grasp Quality**: Each ground-truth positive grasp
from the Cornell Grasping Dataset as a binary label and set
the corresponding area of Q_T to a value of 1. All other pixels
are 0.

**Angle**: The angle of each grasping rectangle
in the range [−π/2,π/2], and set the corresponding area of ΦT .
We encode the angle as two vector components on a unit
circle, producing values in the range [−1, 1] and removing
any discontinuities that would occur in the data where the
angle wraps around ±π/2 if the raw angle was used, making
the distribution easier for the network to learn [9]. Because
the antipodal grasp is symmetrical around ±π/2 radians, we
use use two components sin(2Φ_T) and cos(2Φ_T) which provides values 
which are unique within Φ_T ∈ [−π/2,π/2] and symmetrical at ± π/2
.

![](images/input_output.png)


##Dataset
We use cornell grasp dataset in this task. The dataset can be found here:
https://www.kaggle.com/datasets/oneoneliu/cornell-grasp

##Evaluation

