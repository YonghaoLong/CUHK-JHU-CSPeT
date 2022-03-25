# CUHK-JHU Cross-Site Peg Transfer Dataset (CUHK-JHU CSPeT) Description

## [Project page](https://drive.google.com/drive/folders/1tklk7GH4OE9P8TKhESRAYVu0LmnYoCMV) and [download link](https://appsrv.cse.cuhk.edu.hk/~yhlong/mrgnet.html). 

## Task

Peg transfer.

Annotation:

    0--A1: Idle (No action performed); 
    1--A2: Reach for peg (with left hand); 
    2--A3: Lift peg (with left hand); 
    3--A4: Exchange (transfer the peg to right hand); 
    4--A5: Place peg (with right hand).

## Data size

### CUHK: 12 trials (12 AVI videos, 12 kinematics txt files).
### JHU: 12 trials (12 rosbag files).

## Data format

### CUHK:

Kinematics format: 

    position x, position y, position z, velocity x, velocity y, velocity x, rotation x, rotation y, rotation z, jaw state

Video format: 

    AVI videos, MPEG-4 encoder, 30Hz

### JHU:
ROS Bag Topics:

    /PSM1/jacobian_spatial                         : std_msgs/Float64MultiArray
    /PSM1/position_cartesian_current               : geometry_msgs/PoseStamped 
    /PSM1/state_jaw_current                        : sensor_msgs/JointState    
    /PSM1/state_joint_current                      : sensor_msgs/JointState    
    /PSM2/jacobian_spatial                         : std_msgs/Float64MultiArray
    /PSM2/position_cartesian_current               : geometry_msgs/PoseStamped 
    /PSM2/state_jaw_current                        : sensor_msgs/JointState    
    /PSM2/state_joint_current                      : sensor_msgs/JointState    
    /jhu_daVinci/left/decklink/camera/image_raw    : sensor_msgs/Image         
    /jhu_daVinci/right/decklink/camera/image_raw   : sensor_msgs/Image


## Data processing script

JHU data process: [https://github.com/JieYingWu/dvrk_action_embedding/](https://github.com/JieYingWu/dvrk_action_embedding/).

## Citation

If you use the dataset, please cite the following paper.

      @inproceedings{
      long2021relational,
      title={Relational graph learning on visual and kinematics embeddings for accurate gesture recognition in robotic surgery},
      author={Long, Yonghao and Wu, Jie Ying and Lu, Bo and Jin, Yueming and Unberath, Mathias and Liu, Yun-Hui and Heng, Pheng Ann and Dou, Qi},
      booktitle={2021 IEEE International Conference on Robotics and Automation (ICRA)},
      pages={13346--13353},
      year={2021},
      organization={IEEE}
      }

