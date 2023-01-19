# basalt_wrapper

This package wraps a modified version of the [Basalt VIO
library](https://gitlab.com/VladyslavUsenko/basalt) with a package.xml and
a CMakeLists.txt file such that it builds with ROS tools (catkin / ament). It
also sets some cmake options for the Basalt package to export
correctly.

This package is a dependency of the [Basalt
ROS](https://github.com/berndpfrommer/basalt_ros) package.

## Platforms

Should be working on Ubuntu 20.04 and 22.04. Not tested for older systems.

## How to build

Install vcstool and bzip2-dev:
```
sudo apt install python3-vcstool libbz2-dev
```

Create a workspace (e.g. ~/ws), clone this repo and fetch.
The ``vcs import`` will run a long while.
```
mkdir -p ~/ws/src
cd ~ws
git clone https://github.com/berndpfrommer/basalt_wrapper.git src/basalt_wrapper
vcs import --recursive < src/basalt_wrapper/basalt_wrapper.repos
```
Build:
```
colcon build --symlink-install --cmake-args -DCMAKE_BUILD_TYPE=RelWithDebInfo
```

## License

This software is issued under the Apache License Version 2.0.
