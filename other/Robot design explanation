Mobility and Mechanical Design

Our robot uses rear-wheel drive with a differential and an Ackermann steering system. We chose this design because it allows smoother and more accurate turns. The differential helps the wheels rotate at different speeds during turns, which reduces slipping. Ackermann steering improves the turning trajectory, especially on tight corners.

We also tested a tank drive system, but it was less stable and caused more errors due to slipping, so we decided not to use it.

The main trade-off is that Ackermann steering is harder to build and requires careful calibration. However, it gives better control and consistency.

We tested different speeds and turning angles to improve alignment before turns and reduce mistakes during navigation.


Power and Sensor Architecture

Our robot uses two ultrasonic sensors placed at the front sides and one gyro sensor in the center.

The side placement of ultrasonic sensors helps detect walls earlier and adjust the path in advance. The gyro sensor is placed in the center to reduce noise and improve accuracy.

We tried to balance accuracy and energy consumption. Adding more sensors could improve precision, but it would also increase power usage and processing delay.

We calibrate the gyro before each run and apply simple filtering to ultrasonic data to reduce noise.

If one sensor gives unstable readings, the robot relies on the other sensors to maintain stable behavior.


Software Architecture and Strategy

The program is divided into simple modules: movement control, sensor processing, and decision-making.

We use a state-based approach:

* moving forward
* preparing for a turn
* turning
* realigning

This makes the robot’s behavior easier to understand and debug.

We also considered edge cases, such as incorrect sensor readings or sudden obstacles.

To evaluate performance, we focused on:

* number of successful laps in a row
* turning accuracy
* lap time

⸻

Systems Thinking and Engineering Decisions

We treated the robot as a connected system where mechanics, sensors, and code all affect each other.

For example, mechanical design affects how accurate the sensors are, and sensor accuracy affects the control algorithm.

We made decisions based on stability rather than maximum speed.

Some risks we identified include gyro drift, ultrasonic delay, and accumulated error over time.

To reduce these risks, we use calibration, simple filtering, and limit extreme movements.
