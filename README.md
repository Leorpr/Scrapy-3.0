# WRO-future engineers 
scrapy

## Engineering Materials
All the materials used to create our robot
- one lego ev3 brick
- one lego ev3 large motor
- one lego nxt large motor
- lego ev3 battery
- spare lego technic pieces


## Contents
- [Models](models/) This directory contains all used 3d models
- [Other](other/) This directory is empty for now, as no miscellancious files have had to be added
- [Process](process/) This directory will be completed for the national as it will contain the process that it took for us to get there
- [Schemes](schemes/) All wiring diagrams can be found in this directory
- [Source Code](src/) This directory contains all the code used in this proyect
- [Team Photos](t-photos/) The official Team photos can be found here
- [Performance Videos](p-videos/) The robot Performance videos 
- [Vehicle Pictures](v-photos/) All vehicle photos can be found in this directory, including some individual components


## Introduction
Brief intro on our solution

As for now, we just got a new robot and had to change our strategy. With this new EV3 robot, we are keeping it as simple as possible, ensuring that the complexity of the tasks does not overwhelm the system or our time constraints. This approach helps us maintain focus on achieving consistent results, even with limited resources and time.

For the first round, the robot will start its tasks with a basic, yet effective, strategy designed to maximize our chances of success.



## strategy
For the first challenge, we have programmed the robot to move the steering completely to the left and then back the same number of degrees to the right so that it is perfectly aligned. This initial movement is crucial as it ensures that the robot starts from a neutral, centered position, allowing for more accurate and reliable navigation. Then, the robot is programmed to adjust the steering to an exact position using degrees, giving us fine control over its movement. This precision will allow us to earn the maximum number of points, even without having the resources to implement a more complete and complex programming due to the lack of time and connector cables. However, this solution is only temporary, and we are already working on another method that could provide even better results in the future. We also considered counting the rotations to obtain the three points achievable after completing the three laps in the initial square. However, this has proven not to be very viable due to small changes such as the robot’s positioning at the start or the condition of the track, which varies from competition to competition. The imperfections in the track can affect the robot’s performance, making it less reliable. Additionally, the battery level affects the number of necessary rotations, so we have discarded this option, at least for this competition. The variability introduced by these factors makes the rotation-based strategy less predictable and, therefore, less desirable for a competition setting where consistency is key.

For the second round, we currently do not have a clear solution due to the lack of connector cables, which limits our ability to fully implement our preferred strategies. However, we do have a strategy in mind that could work well under these constraints. We would use two color sensors at angles of 60 degrees and 120 degrees, respectively, and two ultrasonic sensors on each side of the robot. The robot would advance by checking the distance between the walls, staying in the center of the track by maintaining a distance of at least 40 cm from each wall. This method allows the robot to navigate effectively without veering too close to the edges, which could cause issues with obstacle detection or avoidance. With a low speed and the two color sensors, it should be able to detect obstacles, avoid them on the respective side, and return to the initial position. Another solution for this challenge, or a variation of the previous one, would be to use a gyroscope sensor so that the robot can follow a straight line along a pre-established path and return to it even after deviating to avoid an obstacle. The gyroscope could provide the stability needed to ensure that the robot remains on course, even when external factors like obstacles or uneven surfaces come into play.


## mobility
Our robot uses two motors, one NXT motor for the steering. This motor is coupled to a bar along with a gear that acts as an axle to operate the steering gear. We chose this mechanism because it allows a wide range of motion, which is necessary to execute our strategy, as it is more precise and allows the steering to be positioned exactly at the angle needed to complete the three laps. The precision offered by this setup is critical for ensuring that the robot can navigate the course accurately, especially when tight turns or complex maneuvers are required.

In the rear part of the robot, there is an EV3 motor that is used for forward movement. It is positioned vertically to occupy the least space possible, making the robot compact and rigid. This compact design not only saves space but also contributes to the overall stability of the robot, reducing the likelihood of tipping or other stability-related issues during operation. The vertical positioning of the motor also helps in maintaining a low center of gravity, which is beneficial for handling the robot on uneven surfaces or during sudden changes in direction.


## Code Explanation
First, it is important to clarify that this robot is programmed using the default EV3 software, EV3-G, a block-based programming environment. This environment is particularly user-friendly, allowing us to quickly and efficiently develop the necessary code for our robot. It can also be programmed with Python, Scratch, and Java (using LeJOS), offering greater flexibility depending on the user’s level of expertise and the specific requirements of the project. However, given the limited time, we opted to use EV3-G as we considered it the simplest and fastest option for our needs. The block-based nature of EV3-G made it easier to implement our strategies without needing extensive coding knowledge or experience, which was essential given our time constraints.

The code in this project is fairly simple but effective. We start with moving motor A 200º at a power of 10; this is the first part of the calibration process. By reaching the maximum range of steering movement, this gives us an equal starting point for all programming. This step is crucial because it standardizes the robot’s initial position, ensuring that all subsequent movements are consistent and predictable. Then, it will turn 205º to the right with a power of 10. By making this movement from the maximum steering point, it will be in a straight position, ready to move to any point needed in the different quadrants. This alignment process ensures that the robot is always in the correct orientation before it begins any task, reducing the risk of errors. Then, in a loop, the rear motor will start moving with a power of 60. We decided on this speed because it allows the steering to be more precise and avoids accidents while moving at a good pace, preventing excessively high times. The chosen speed strikes a balance between accuracy and efficiency, allowing the robot to complete its tasks within the allotted time while minimizing the risk of collisions or other mishaps.


## Electromechanical Components
Power Source
In this robot, we are using the EV3 rechargeable battery. It is a 7.4V 2050 mAh lithium-ion (Li-Ion) unit, designed to provide longer duration and convenience compared to traditional AA batteries. This type of battery allows the EV3 brick to operate for longer periods, which is especially useful in this competition where consistent performance is crucial. The battery recharges directly inside the brick using a power adapter, eliminating the need to remove the battery to recharge it. This feature not only saves us time and effort but also ensures that the robot remains fully assembled and ready to go at all times. By not having to disassemble the robot to change batteries, we reduce the chances of introducing assembly errors or damaging components during reassembly. Additionally, the EV3 brick includes a charge level indicator, making it easier to manage power and ensuring that the robot is always ready to operate. This indicator is particularly useful during competitions, where knowing the battery level at a glance can be critical for planning and executing strategies. Overall, the EV3 rechargeable battery offers significant advantages in terms of both convenience and performance, making it an ideal choice for our robot in this competition setting.


