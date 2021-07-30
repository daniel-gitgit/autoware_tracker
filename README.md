# Readme

Barebone package for point cloud object tracking used in Autoware. 
The package is only tested in Ubuntu 16.04 and ROS Kinetic by the original author. 
Attempt to set up with Ubuntu 20.04 and ROS Noetic.
No deep learning is used.

# Install JSK
```
sudo apt-get install ros-noetic-jsk-recognition-msgs
sudo apt-get install ros-noetic-jsk-rviz-plugins
```

# Compile
```
#cd ~/catkin_ws/src
#git clone https://github.com/TixiaoShan/autoware_tracker.git
cd ~/catkin_ws
catkin build autoware_tracker -j1
```
```-j1``` is only needed for message generation in the first install.

# Sample data

In case you don't have some bag files handy, you can download a sample bag using:
```
wget https://autoware-ai.s3.us-east-2.amazonaws.com/sample_moriyama_150324.tar.gz
```

# Demo

Run the autoware tracker:
```
roslaunch autoware_tracker run.launch
```

Play the sample ros bag:
```
rosbag play sample_moriyama_150324.bag
```

<p align='center'>
    <img src="/launch/demo.gif" alt="drawing" width="800"/>
</p>