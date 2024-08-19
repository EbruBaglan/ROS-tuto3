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

## 4.2.1.
how it came about
Kalman Filter... localization challenges...why filter need. start with 1D example, move to multi dim example... both in C++... extended kalman filter with additional applications

4.2.2.
Kalman filter is an estimation algorithm...pos/vel of a robot or temp. of process...note worthy... uncertainty or noise and give estimate so fast... state prediction and measurement update cycle...
What does it take as an input, what does it filter out, and what important substance does it let through? The graphic below compares a household coffee filter, an engineering low-pass filter, and a Kalman filter. graph.

4.2.3
trajectory estimation in apollo 
introduced it to NASA...trajectory estimation of Apollo program...(Stanley Schmidt)
accurate enough and small enough to run on onboard comp

measurements coming in irregular time intervals

4.2.4.
estimate state when measurements are noisy. engineering and economics... feature tracking...

4.2.5.
KF- linear
EKF - nonlinear
UKF - highly nonlinear (unscented KF)...where EKF may not converge

4.2.6.
go for 10m
bell curve...gaussian...specific to robot and environment...

4.2.7.
help us better sense...a few sensor measurements... initial guess...expected uncertainty of a sensor/movement... GPS data...accurate to few meters...additional sensors onboard... sensor fusion... uses Kalman filter...

4.2.8.
At the basis of the Kalman Filter is the Gaussian distribution, sometimes referred to as a bell curve or normal distribution. Recall the rover example - after executing one motion, the rover’s location was represented by a Gaussian. It’s exact location was not certain, but the level of uncertainty was bounded. It was unlikely that the rover would be more than a few meters away from its target location, and it would be nearly impossible for it to show up at the 50 meter mark.

Mean and Variance

A Gaussian is characterized by two parameters - its mean (μ) and its variance (σ²). The mean is the most probable occurrence and lies at the centre of the function, and the variance relates to the width of the curve. The term unimodal implies a single peak present in the distribution.

Gaussian distributions are frequently abbreviated as N(x: μ, σ²), and will be referred to in this way throughout the coming lessons.

That’s right, the Kalman Filter treats all noise as unimodal Gaussian. In reality, that’s not the case. However, the algorithm is optimal if the noise is Gaussian. The term optimal expresses that the algorithm minimizes the mean square error of the estimated parameters.

4.2.9.
internal belief... best guess...
state(x), measurement(z), control action(u)... yaw... 3 state variables...
Kalman filter cycle: initial estimate of state, state prediction, measurement update...

4.2.10.
Quizzes

4.2.11.
Position + Motion

4.2.12


-->
