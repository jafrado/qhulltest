# qhulltest
Test QHull library with PCL, perform RANSAC GPF, Convex Hull and Pyramidal Extraction

## Prerequisites

PCL with VTK and QHull installed
```
C:\vcpkg>vcpkg install vtk[qtopengl] --triplet x64-windows
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

## Output

The PCL viewer will start, press "r" to recenter the point cloud. Use the wheel mouse to zoom in and out, and press center / left button amd move mouse to change the view.

