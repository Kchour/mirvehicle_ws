# Properties

## Conversion Table from catvehicle to mirvehicle

| CAT           | value    | MIR (bulldogbolt) | value  | unit | Meaning                       |
|---------------|----------|---------------|--------|------|-------------------------------|
| base_height   | 1.0639   | base_height   | 1.0639 | m    | The height of the base frame  |
| base_mass     | 2050     | base_mass     | 1625   | kg   | The weight of body (wheels?)  |
| base_mass_ixx | 63       | base_mass_ixx | 63     | N/A  | The base inertia for ixx      |
| base_mass_iyy | 1048     | base_mass_iyy | 1048   | N/A  | The base inertia for iyy      |
| base_mass_izz | 1111     | base_mass_izz | 1111   | N/A  | The base inertia for izz      |
| base_mass_ixz | -31      | base_mass_ixz | -31    | N/A  | The base inertia for ixz      |
| tyre_x        | 1.31     | tire_x        | wheelbase/2    | m    | The relative x position of a tire w.r.t the center of the base. The half of the wheelbase |
| tyre_y        | 0.765    | tire_y        | track_width/2 | m    | The relative y position of a tire w.r.t. the center of the base. The half of the track  |
| tyre_length   | 0.229    | tire_length    | 0.215  | m    | The tire section width        |
| tyre_r        | 0.66     | tire_diameter | 0.6468 | m    | 215/50R17 for Chevy Bolt. 0.215 x 0.5 x 2 + 0.4318(17")  |
| tyre_radius   | 0.356    | tire_radius   | 0.3234 | m    | The half of `tire_diameter`   |
| tyre_mass     | 40       | tire_mass     | 40     | kg   | The tire mass including rim   |
| tyre_mass_ixx | 54       | tire_mass_ixx | 54     | N/A  | The tire inertia for ixx      |
| tyre_mass_iyy | 56       | tire_mass_iyy | 56     | N/A  | The tire inertia for iyy      |
| tyre_mass_izz | 104      | tire_mass_izz | 104    | N/A  | The tire inertia for izz      |
| car_height    | 1.4478   | car_height    | 1.594  | m    | The height of the car         |
| car_to_bumper | 2.4      | dist_to_bumper| 2.2?   | m    | The distance from the center of the base to the bumper  |
| front_bumper_height | car_height/2 | front_bumper_height | m | car_height/2 | The height of the front bumper |
| sensor_box    | 0.25     | sensor_box    | 0.25?  | m    | The sensor box is a cube. The size of an edge   |
| sensor_box2   | 0.31     | N/A           | N/A    | m    | NOT USED   |
| camera_box    | 0.1      | camera_box    | 0.1    | m    | The camera box is a cube. The size of an edge   |
| tyre_height   | -0.696   | N/A           | N/A    | m    | NOT USED   |
| str_length    | 0.01     | steer_length  | 0.01   | m    | The height of steering link (cylinder shape)  |
| str_radius    | 0.1      | steer_radius  | 0.1    | m    | The radius of steering link (cylinder shape)  |
| str_angle     | 0.6      | steer_angle_limit | 0.6 | m    | The maximum angle of steering |
|               |          | wheelbase     | 2.6    | m    | The wheelbase                  |
| car_width     | 1.301    | track_width   | 1.501  | m    | The track width                |
| car_width     | 1.301    | car_width     | 1.765  | m    | The car width                  |
|               |          | car_length    | 4.166  | m    | The car length                 |

## Notes

In the catvehicle, `car_width` is used as both the `track width` and the vehicle's width. Be careful to change it in the URDF files.