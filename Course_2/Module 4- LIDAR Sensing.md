# Light Detection and Ranging Sensors

LIDAR sensors use lasers pulses and time-of-flight to measure distances to objects along a specific direction. For 2D or 3D LIDARs work by sweeping the laser pulses in many directions across the whole environment.
Considering the operation of a LIDAR, we should be aware of some sources of measurement noise:

- Uncertainty in determining the exact time of arrival of the reflected signal.
- Uncertainty in measuring the exact orientation of the mirror.
- Interaction with the target (ex: surface absorption)
- Variation of propagation speed.

Also, for a moving vehicle, each point in a scan is taken from a slightly different place. We need to take this into account, otherwise, for a quickly moving vehicle, the motion distorsion can become a problem.

# LIDAR Sensor Models and Point Clouds

We will need to do 3 operations on Point Clouds:

- Translation
- Rotation
- Scaling

For this, we will use a data structure like this:

We assign an index to each of the points, say point 1 through point n, and store the x, y, z coordinates of each point as a 3 by 1 column vector. We stack them side by side into a matrix that we'll call big P. Doing it this way make it easier to work with the standard linear algebra libraries, like the Python NumPy library, which lets us take advantage of fast matrix operations.

For doing basic and advanced operations on point clouds, we have the open-source Point Cloud Library (PCL) built with C++ but it exists unofficial python binding available.

# Pose Estimation from LIDAR Data

To determine the motion of a self-driving car by aligning points clouds from LIDAR, we use ICP (Iterative Closest Point) algorithm. It works by iteratively minimizes the distance between points in each point clouds.

Moving objects violate the stationary world assumption that ICP is based on, so it can be a problem. These outlier measure can be mitigated by using Robust Loss Functions which assign less weight to large errors than the usual squared error loss.
