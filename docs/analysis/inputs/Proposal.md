The Freenove Smart Car was chosen as a raspberry pi platform for introducing interns to embedded software and artificial intelligence concepts.  Taking advantage of the sensors and peripherals provided by the platform, the following projects were determine to provide an adequate introduction within the time afford the projects.  Each project is tailored for a one week duration allowing interns time to both meet project objectives along with completing the other tour, panels, and briefings there are assigned.

The Freenove Smart Car provides sample python client and server code for implementing line tracking, object avoidance, face tracking, utilizing the LEDs, and other features.  
(Note: The code provided by Freenove contains updates supporting a newer camera.  The picamera2 import and respected code needs to be reverted to utilize the legacy picamera libraries.)
[P001] The requirement for each of the following projects is to implement the functionality in the raspberry pi.  Outside of any code for starting, stopping, resetting, etc., the functions performing the below requirements should reside in the car.  
[P002] The application shall use Python
[P003] The application shall use YOLO for its AI object detection engine
[P004] Deliverables shall include source code git repository, install instructions (pip, apt, etc.), scripts used to train AI model

The car shall do the following:
1. Navigate a course by utilizing the infrared sensor to perform boundary detection and stay within the course (Note: boundary detection and not line tracking)
2. Car shall stop when the ultrasonic sensor detects an object which can be placed at the end of the track.
3. When the software detects a ball within one foot, the car shall perform the following activities:
 -	Determine color of ball and change vehicle LEDs to match color of ball.
 -  Drive car into ball to knock ball outside the boundary.  If ball remains inside boundary, application should continue attempting to knock ball outside of boundary until a boundary wall is detected.
 -	Pause the car for five seconds before continuing down the track.
 -	Flash LEDs to indicate condition has been met prior to transitioning to next ball in sequence.  LEDs should reset to off once after three seconds.
4. Once a ball color is detected and pushed off the boundary, the application shall ignore that color ball for the remainder of the program.
