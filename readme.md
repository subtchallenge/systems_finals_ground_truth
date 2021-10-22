# README #

This repo provides ground truth data for Artifact types and locations used at the DARPA Subterranean Challenge Final Event. It also includes various data products that may be of interest to the SubT Challenge Community.

### Files ###

* Systems_Finals_Artifact_Ground_Truth.xlsx -- Spreadsheet listing each Artifact; its type; and x,y,z location in the DARPA coordinate frame.
* Systems_Finals_Fiducials_Ground_Truth.xlsx -- Spreadsheet listing reference frame fiducials defining the DARPA coordiante frame.
* data/systems_final.pcd -- Down-sampled point cloud of the Finals course, defined in the DARPA Cartesian coordinate frame.
* Systems_Finals_Artifacts_Map_<round>.pdf -- Maps of Artifact locations and associated artifact types for all rounds together and the three rounds individually.
* course_design/Finals_Course_Callouts.pdf -- Details the design of each section of the Final Event competition course. Each section description includes design parameters, fabrication details, inspiration references, and pictures of both the build and the virtual model.
* course_design/Finals_Course_Graphics.zip -- Zip file with many of the artwork and graphics used in the Final Event competition course. 

### Course Visualization in RViz ###

The course may be visualized as a point cloud with artifact markers using ROS and RViz. This package depends on ROS and the `pcl_ros` package to build.

To visualize the point clouds and artifact locations, run `roslaunch finals_ground_truth view.launch`. Pass with argument, e.g., `config:=prelim1` to visualize artifact locations for a particular configuration. The default configuration is `prize`. Config may be `prelim1`, `prelim2`, or `prize`.

### Note on Coordinate Transforms ###

Surveyed scan data is provided in a single file.
When using the *view.launch* file, the point cloud is provided in the `darpa`
coordinate frame with transformations between `darpa`, and `utm` frames provided
on the */tf_static* ROS topic. These coordinate frames are defined as follows:

* `darpa` = the DARPA Cartesian coordinate frame for the Finals course

* `utm` = a Cartesian coordinate frame, defined by UTM zone 16N

### Additional Links ###

* **Point Cloud Flythrough Videos**
  * Tunnel Flythrough: https://youtu.be/0brZuy6Qq2E
  * Urban Flythrough: https://youtu.be/odE8a-5CW6A
  * Cave Flythrough: https://youtu.be/uXaj_M6L5oo

* **Course Walkthrough Videos**
  * Prelim 1: https://youtu.be/i-8aPpJfGS0
  * Prelim 2: https://youtu.be/zqRuBJ-VxMg
  * Prize Round: https://youtu.be/6Fte0KipSfk 

* **Full Run Videos Playlist**
  * Final Event full run videos: https://youtube.com/playlist?list=PL6wMum5UsYvZd6VwOZVZHu9QldFp8vEgX


