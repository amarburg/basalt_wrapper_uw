# basalt_wrapper

This package wraps a modified version of the [Basalt VIO
library](https://gitlab.com/VladyslavUsenko/basalt) with a package.xml and
a CMakeLists.txt file such that it builds with ROS tools (catkin / ament). It
also sets some cmake options for the Basalt package to export
correctly.

## How to build

Create a workspace (e.g. ~/ws), clone this repo and fetch:
```
mkdir -p ~/ws/src
cd ~ws
git clone https://github.com/berndpfrommer/basalt_wrapper.git src/basalt_wrapper
vcs import --recursive < src/basalt_wrapper/basalt_wrapper.repos
```
Build:
```
colcon --DCMAKE_BUILD_TYPE=RelWithDebInfo
```

## License

This software is issued under the Apache License Version 2.0.
