# mirvehicle_ws

This MIR(Mobile Intelligent Robotics Lab) Vehicle workspace has been prepared to create a working environment for the Kettering University's Bulldog Bolt for SAE's AutoDrive Changllenge. 

## Contributors

* Jaerock Kwon, Ph.D. Associate Professor
* Shobit Sharma, Research Assistant
* Mohamed Fasil Syed, Research Assistant

## Folder Structure

* `mirvehicle`: ROS nodes will be located.
* `mirvehicle_description`: vehicle model. It includes `urdf` and `meshes`. There is a single launch file in `launch` folder. `bulldogbolot_state_publisher.launch` will start `rviz` with the config file, `bulldogbolt_state_publisher.rviz`. This is used to verify that the vehicle's urdf model are well made.
  * `bulldogbolt`: A specific vehicle model name. Under this folder, you must define a vehicle's model.
    * `main.urdf.xacro`: The main urdf. This will be called by launch files. This main urdf includes following three xacros.
    * `properties.urdf.xacro`: This defines the properties of the vehicle. You may need to change this to specify a vehicle model's properties.
    * `structure.urdf.xacro`: This defines the vehicle's body and wheels.
    * `sensors.urdf.xacro`: This defines cameras and laser sensors.
* `mirvheicle_gazebo`: This is for Gazebo simulation.
  * `config/bulldogbolt_control.yaml`: controller defintions.
  * `launch`
    * `bulldogbolt_empty.launch`: Start the Gazebo server with Bulldogbolt model and a basic world. You need to start `gzclient` in a separate terminal if you want to use Gazebo.
    * `bulldogbolt_gazebo.launch`: Start the Gazebo server and client. This will start `rviz` as well to visualize sensor data. You can use a parameter input for a world name. Use `world:=<world_name>` where the world name can be found at `world` folder. The default world name is `skidpan`. 
    * `bulldogbolt_neighborhood.launch`: This is same as `bulldogbolot_gazebo.launch world:=neighborhood`
    * `mirvehicle.launch`: This is a generic launch file that will be included by other launch files. There is no need to use this launch file directly.

  * `models`: 3D object models for Gazebo.
  * `worlds`: World files for Gazebo.

## Acknowledgements

This project was possible with the generous works of Arizona University's the CAT Vehicle Testbed and Dataspeed Inc's ADAS system (dbw_mkz).