# qhulltest
Test QHull library with PCL, perform RANSAC GPF, Convex Hull and Pyramidal Extraction

## Prerequisites

PCL with VTK and QHull installed
```
C:\vcpkg>vcpkg install vtk[opengl] --triplet x64-windows
C:\vcpkg>vcpkg install pcl[opengl] pcl[qt] pcl[pcap] pcl[tools] pcl --triplet x64-windows
```

Tabletop/Planar Pointcloud

[countertop.zip](https://sourceforge.net/projects/pointclouds/files/PCD%20datasets/countertop.zip)

## Building

Unix
```
cd qhulltest; mkdir build; cd !$ && cmake ..
make
```
Windows
```
devenv /rebuild Release qhull_gpf_test.sln
```

## Running

Issue the command below on your favorite Point cloud:

```
 ../build/Release/qhull_gpf_test 9.pcd
Planar segmentation:55854 points
Convex hull:23 points
Prism:37101 points
```

The PCL viewer will start, press "r" to recenter the point cloud. Use the wheel mouse to zoom in and out, and press center / left button amd move mouse to change the view. See below for details:

![alt text](https://github.com/jafrado/qhulltest/raw/master/qhull.jpg "Qhull Test Example")



