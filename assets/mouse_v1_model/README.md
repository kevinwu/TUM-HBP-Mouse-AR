# MouseModel

This folder contains a first version of the mouse kinematics in URDF based on the blender mouse model. To visualize the URDF model with the ROS hydro default installation, use the following command:
```
source /opt/ros/hydro/setup.bash
cd <PATH_OF_THIS_README>
roslaunch urdf_tutorial display.launch model:=model.urdf 
```

To check the correctness of the URDF file the URDF checker can be used:
```
check_urdf model.urdf
```

The URDF model can be easily translated into a SDF model for the GAZEBO simulator by
```
gzsdf print model.urdf > model.sdf
```
Important is the specifiaction of an inertia element for each link!


To open the SDF mouse model with gazebo copy this folder to ~/.gazebo/models. After starting GAZEBO the mouse model is available in the models list.

Axel von Arnim, September 2015:
In model.sdf, the cameras were adjusted to diverge a bit from the straight line in front of the camera. Beware to replicate that in case you modify the SDF.