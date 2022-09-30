# Project
Flying a drone over some terraing and to construct a 3D model of that terrain.

<!-- TABLE OF CONTENTS -->

## Table Of Contents
* [Project](#project)
  * [Table of Contents](#table-of-contents)
  * [About The Project](#about-the-project)
    * [Tech Stack](#tech-stack)
    * [File Structure](#file-structure)
  * [Getting Started](#getting-started) 
    * [Prerequisites and installlation](#prerequisites-and-installlation)
    * [Installation](#installation)
    * [Execution](#execution)
  * [Algorithm Flowchart](#algorithm-flowchart)
  * [Results and Demo](#results-and-demo)
  * [Future Work](#future-work)
  * [Contributors](#contributors)
  * [Acknowledgements and Resources](#acknowledgements-and-resources)
  * [License](#license)

## About the Project

* The idea is to have a Drone fly over some terrain in ROS with a GPS and a Depth sensor, then get the pointcloud data from the drone and create a 3D map of the topography of the terrain. 
* The main aim of the project is to learn about surface reconstruction of pointcloud data involving techniques such as subsampling and various algorithm for mesh creation.

### Tech Stack
* [ROS Noetic](http://wiki.ros.org/noetic)
* [Gazebo](http://gazebosim.org/)
* [Point Cloud Library](https://pcl.readthedocs.io/en/latest/)

### File Structure
```
📦Eklavya---Drone-3D-Topography
 ┣ 📂assets                           #contains gifs, videos and images of the results
 ┣ 📂config                           #Rviz config files
 ┣ 📂include                          #include files for the plugins
 ┃ ┗ 📜DialogKeyboard.h  
 ┃ ┗ 📜drone_object_ros.h             
 ┃ ┗ 📜pid_controller.h             
 ┃ ┗ 📜plugin_drone.h             
 ┃ ┗ 📜plugin_ros_cam.h             
 ┃ ┗ 📜plugin_ros_imu.h             
 ┃ ┗ 📜plugin_ros_imu_native.h
 ┃ ┗ 📜plugin_ros_sonar.h
 ┃ ┗ 📜sensor_model.h
 ┃ ┗ 📜util_ros_cam.h                 
 ┣ 📂launch                           #launch files
 ┃ ┗ 📜simple.launch
 ┣ 📂models                           #files and meshes used to render the model                       
 ┃ ┗ 📂kinect
 ┃ ┃ ┣ 📂materials
 ┃ ┃ ┣ 📂meshes
 ┃ ┃ ┣ 📜model.config
 ┃ ┃ ┗ 📜model.sdf
 ┣ 📂plugins                         #plugins for the model
 ┃ ┗ 📜libplugin_drone.so
 ┃ ┗ 📜libplugin_ros_cam.so             
 ┃ ┗ 📜libplugin_ros_imu.so           
 ┃ ┗ 📜libplugin_ros_sonar.so          
 ┣ 📂scripts                          #C++ program used to run the drone
 ┃ ┣ listener.cpp                     #Used to get PCD from the drone and to process the data using PCL
 ┣ 📂src                              #contains custom plugins used with the drone
 ┃ ┣ 📜DialogKeyboard.cpp
 ┃ ┗ 📜DialogKeyboard.ui
 ┃ ┗ 📜drone_keyboard.cpp
 ┃ ┗ 📜drone_object_ros.cpppid_controller.cpp
 ┃ ┗ 📜plugin_drone.cpp
 ┃ ┗ 📜plugin_ros_cam.cpp
 ┃ ┗ 📜plugin_ros_imu.cpp
 ┃ ┗ 📜plugin_ros_imu_native.cpp
 ┃ ┗ 📜plugin_ros_init.cpp
 ┃ ┗ 📜plugin_ros_sonar.cpp
 ┃ ┗ 📜util_ros_cam.cpp
 ┣ 📂urdf
 ┃ ┗ 📜sjtu_drone.urdf
 ┣ 📂worlds                           #world files
 ┃ ┣ 📜terrain.world
 ┣ 📜CMakeLists.txt
 ┣ 📜README.md
 ┗ 📜package.xml
 
 ```
 
 ## Getting Started
 
 ### Prerequisites and Installlation
 
* Tested on [Ubuntu 20.04](https://ubuntu.com/download/desktop)
* [ROS Noetic](http://wiki.ros.org/noetic/Installation)
* [Gazebo Sim](http://gazebosim.org/)
* Do visit these websites for the installation steps of the above mentioned software. It is recommended to install Gazebo along with ROS and not seperately
 
### Installation

```sh
git clone https://github.com/Shazam213/Drone-3d-topography.git
```


 
 
 
 
 <!-- CONTRIBUTORS -->
## Contributors
* [Soham Mulye](https://github.com/shazam213)
* [Unmani Shinde](https://github.com/unmani-shinde)
