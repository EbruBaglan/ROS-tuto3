# ROS-tuto3
<!--
## 4.1.1.
1. Localization: determining the robot's pose in a mapped environment. done by implementing a probabilistic algorithm to filter noisy sensor measurements and track the robot's position and orientation.
4 very popular localization algorithms:
1. EKF: the most common Gaussian filter that helps in estimating the state of a nonlinear models.
2. Markov Localization: base filter localization algorithm. maintaind a probability distribution over the set of all possible position and orientation the robot might be located at.
3. Grid localization: histogram filter >> capable of estimating the robot's pose using grids
4. Monte Carlo localization: particle filter, estimates robots pose using particles

EKF and MCL: Monte Carlo localization.

Textbook: Probabilistic Robotics(opens in a new tab) by Sebastian Thrun,‎ Wolfram Burgard,‎ and Dieter Fox.
Udacity's AI for Robotics(opens in a new tab) Free Course

## 4.1.2.
2 things that determine the difficulty of the localization task:
  1. the amount of information present
  2. nature of the environment, the robot is operating in

3 different localization problems that are not all equal. 
  1. Position tracking: local localization. Robot knows its initial position, moves around and estimates its pose. no so easy since there is uncertainty in robot motion. limited to region surrounding the robot
  2. Global localization: robots initial pose is unknown, robot must determine its pose relative to the ground through the map. more difficult than position tracking.
  3. Kidnapped robot: robot might be kidnapped at any point, and put to a new location. worst possible case.

## 4.1.3.
Kalman Filter: filtering noisy sensor data. learn the limitation to overcome, and variations.
Sensor Fusion: in lab. multiple sensor to 
Monte Carlo Localization: uses particle filters to track your robot pose and present many advantages over EKF. How particles can tell a robot's pose. using Adaptive Monte Carlo Localization Package...
  

-->
