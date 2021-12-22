# README #

This repo provides ground truth data for Artifact types and locations used at the DARPA Subterranean Challenge Final Event. It also includes various data products that may be of interest to the SubT Challenge Community.

### Files ###

* Systems_Finals_Artifact_Ground_Truth.xlsx -- Spreadsheet listing each Artifact; its type; and x,y,z location in the DARPA coordinate frame.
* Systems_Finals_Fiducials_Ground_Truth.xlsx -- Spreadsheet listing reference frame fiducials defining the DARPA coordiante frame.
* artifacts/systems_final_<round>.csv -- Text files listing each Artifact type and x,y,z location in the DARPA coordinate frame.
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
 
* **360 Degree Flythrough Video Links**
    * Tunnel: https://youtu.be/G8SLE7phtLY
    * Urban: https://youtu.be/yTecsOv_1Rw
    * Cave: https://youtu.be/DCE59ViPoMY
 
* **Full Run Videos Playlist**
    * Final Event full run videos: https://youtube.com/playlist?list=PL6wMum5UsYvZd6VwOZVZHu9QldFp8vEgX
 
* **Finals Course High Resolution Point Cloud**
    * https://subt-challenge.s3.amazonaws.com/final_event/systems_final_highres.las -- High resolution point cloud with a file size of 12 GB.
    * A full resolution point cloud file is also available upon request (>100 GB). Any teams interested in utilizing the full resolution file may send a request to subtchallenge@darpa.mil.
 
* **Finals Course Mesh Files**
    * https://subt-challenge.s3.amazonaws.com/final_event/Systems_Final_Mesh_FBX.zip -- Meshes in FBX format with a file size totaling 0.4 GB.
    * https://subt-challenge.s3.amazonaws.com/final_event/Systems_Final_Mesh_OBJ.zip -- Meshes in OBJ format with a file size totaling 2.4 GB. 
 
* **Virtual Worlds for each Systems Finals Course Configurations**
    * https://github.com/osrf/subt -- Virtual Worlds for each of the course configurations used in the Systems Final Event
 

* **Point Clouds Sampled from Virtual Worlds**
    * https://github.com/subtchallenge/virtual_ground_truth -- Ground truth point cloud data for each of the Virtual Competition worlds: 
 

* **High Resolution Cave Point Cloud Files**
Scans are also available upon request from several segments of caves that were used as inspiration for the Finals Course cave subdomain. 5 total segments are available and range from 15-60m in length for a total file size of >130 GB. Any teams interested in utilizing the cave scan files may send a request to subtchallenge@darpa.mil.
