## for compile

### for c++
sh build.sh
### for ros
add `export ROS_PACKAGE_PATH=${ROS_PACKAGE_PATH}:/home/kadn/github/ORB_SLAM2_SAVEMAP/Examples/ROS`  to your .bashrc
```
source .bashrc
cd YOUR/PATH/TO/ORB_SLAM2_SAVEMAP/Examples/ROS/ORB_SLAM2
mkdir build
cd build
cmake ..
make -j
```

## for use
please prepare ORBvoc.bin or ORBvoc.txt
### save map

```
cd ORB_SLAM22

./Examples/ROS/ORB_SLAM2/Mono Vocabulary/ORBvoc.bin Examples/Monocular/orbbec.yaml false
```

### use an existed map

make sure there is a map named "Slam_Map.bin" in ORB_SLAM22

```
cd ORB_SLAM22

./Examples/ROS/ORB_SLAM2/Mono Vocabulary/ORBvoc.bin Examples/Monocular/orbbec.yaml true
```

## others
- ros_mono is ok for save and load and relocalization.
- ros_rgbd : not yet

## image topics

change code in  ros_mono to decide if you are going to use another topic


## possible problem 

1.`terminate called after throwing an instance of 'boost::archive::archive_exception'`
Please make sure there is a map named "Slam_Map.bin" in your main folder
