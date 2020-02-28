# State Estimation in Practice

In practice, state estimation typically fuses data from multiple sensors like IMUs, LiDAR, cameras, and GPS or GNSS receivers. For a correct sensor fusion, the calibration is very important. We need to consider the relative positions and orientations of all the sensors and any differences in polling time. We need to think about how to safely cope with localization failures and aspects of the world that do not conform to our assumptions such as moving objects.

# Multisensor Fusion for State Estimation

For vehicular state estimation, we use EKF(Extended Kalman Filter). In order to fuse GNSS with IMU and LIDAR measurements.

For this we made some assumption:

- LIDAR provides position in the same reference frame as GNSS.
- IMU has no biases.
- State initialization is provided.
- Our sensors are spatially and temporally aligned.

# Sensor Calibration - A Necessary Evil

Sensor fusion is impossible without calibration, for this, we have to deal with 3 types of calibatrion:

- Intrinsic Calibration: sensors specific parameters.

- Extrinsic Calibration: how the sensors are positioned and oriented on the vehicle.

- Temporal calibration: Time offset between different sensors measurements

# Loss of One or More Sensors

We have seen different examples of car crashing because of a sensor malfunction and a bad management of this failure. For this, multiple sensors are crucial to robust localization in varied environment.
