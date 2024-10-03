
# Advanced Sensor Fusion for State Estimation in Autonomous Systems
## Project Overview
This project focuses on developing advanced sensor fusion techniques for accurate state estimation in autonomous systems. We integrate data from Inertial Measurement Units (IMU) and Global Positioning System (GPS) sensors to achieve high-precision positioning and navigation.

## Key Features

* ROS Driver Integration: Custom ROS driver for seamless integration of IMU and GPS sensors.
* Allan Variance Analysis: Comprehensive stability assessment of IMU data.
* Complementary Filter: Advanced algorithm to combine magnetometer and yaw rate sensor data for improved yaw angle estimation.
* Dead Reckoning Algorithm: Sophisticated positioning technique using IMU data, with bias and drift elimination.
* Real-Time Kinematic (RTK) GPS Integration: High-precision GPS data processing for centimeter-level accuracy.

## Methodology

### Sensor Calibration and Error Correction

* Magnetometer Calibration: Implemented hard-iron and soft-iron error corrections to enhance magnetometer accuracy.
* IMU Bias Correction: Developed methods to identify and remove acceleration bias, particularly during stationary periods.

### Data Fusion Techniques

1. Yaw Angle Estimation:
* Integration of yaw rate sensor data
* Magnetometer-based calculations
* Complementary filter implementation combining low-pass filtered magnetometer data and high-pass filtered gyroscope data


2. Velocity Estimation:
* Integration of bias-corrected IMU acceleration data
* Comparison and alignment with GPS-derived velocity


3. Position Tracking:
* Implementation of dead reckoning using integrated IMU data
* Transformation of velocity into fixed (East, North) reference frame using magnetometer-derived heading

## Results and Performance

* Achieved centimeter-level accuracy in stationary RTK GPS measurements (RMSE: 0.13 cm)
* Improved accuracy in occluded environments (Stationary RMSE: 1.7 cm, Walking RMSE: 2.5 cm)
* Significant improvement in positioning accuracy compared to standalone GPS systems

## Future Work

* Integration with additional sensors (e.g., LiDAR, camera) for enhanced environmental perception
* Implementation of more advanced fusion algorithms (e.g., Extended Kalman Filter, Particle Filter)
* Real-time performance optimization for deployment on autonomous vehicles
