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
# Acknowledgement
This repo is a modified from [this](https://gist.github.com/rotu/1eac858b808b82bbf1b475f515e91636).