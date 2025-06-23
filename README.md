# USAGE
This repo is created to develop ros2 project in clion conveniently.
```
git clone https://github.com/ZiDXie/ros2_top_cmake.git
```
Then copy the CMakeLists to your workspace.
## choose package
In line 44.
```
#    uncomment the following line to select package
#	--packages-select [package name]
```
## build package
Your File Tree should looks like the following
```
├── CMakeLists.txt
│   
└── src
```
If you use colcon build,there's something wrong.Instead,use
```
colcon build --base-paths src/*
```
### another way
Otherwise,you can create a directory like devel_ws.
Then move the src to devel_ws.The file free:
```
├── CMakeLists.txt
│   
└── devel_ws
  ├── src
```
Edit code in line 42 43:
```
BUILD_BASE "${PROJECT_SOURCE_DIR}/devel_ws/build"
BASE_PATHS "${PROJECT_SOURCE_DIR}/devel_ws/src/"
```
Then you can use colcon build in devel_ws.
# Acknowledgement
This repo is a modified from [this](https://gist.github.com/rotu/1eac858b808b82bbf1b475f515e91636).
