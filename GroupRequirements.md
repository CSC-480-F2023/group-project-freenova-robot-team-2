# Format:

### [Condition] [Subject] [Action] [Object] [Constraint]

EXAMPLE: When signal x is received [Condition], the system [Subject] shall set [Action] the signal x received bit [Object] within 2 seconds [Constraint].

Or

### [Condition] [Action or Constraint] [Value]

EXAMPLE: At sea state 1 [Condition], the Radar System shall detect targets at ranges out to [Action or Constraint] 100 nautical miles [Value].

Or

### [Subject] [Action] [Value]

EXAMPLE: The Invoice System [Subject] shall display pending customer invoices [Action] in ascending order [Value] in which invoices are to be paid.
Gather all the feature requirement definitions your team has created into a single document. This document can be as simple as a markdown file that references each of the requirements, stakeholders, and constraints to as formal as a Software Requirements Specification document.

# Requirements: 

[Functional] The application will use Python as the primary coding language 

[Functional] The application will use YOLO for its AI object detection engine

[Functional] The application will be created using a Raspberry Pi platform

[Functional] The application will use a provided sample Python client and server code for implementing line tracking, object avoidance, face tracking, LEDs, and other features. 

[Functional] The application will utilize a camera attachment, an infrared sensor, an ultrasound sensor, and other robotic parts to navigate an obstacle course. 

[Non-Functional] Streaming video to the client application to include object detection bounding boxes as to allow users to see the system work.

[Functional] Deliverables shall include source code git repository, install instructions (pip, apt, etc.), and scripts used to train the AI model.

[Functional] The application will have 4 variations each with different requirements.

## Variation 1 

[Functional] Navigate a course by utilizing the infrared sensor to perform boundary detection and stay within the course (Note: boundary detection and not line tracking)

[Functional] The car shall stop when the ultrasonic sensor detects an object which can be placed at the end of the track.

## Variation 2 

[Functional] The car needs to be able to detect a ball within one foot. 

[Non- Functional] The application shall determine the color of the ball 

[Functional] The application will change the vehicle LEDs to match the color of the ball. 

[Non- Functional] The application will pause the car for five seconds before continuing down the track. 

[Functional] Once a ball color is detected, the application shall ignore that color ball for the remainder of the program.

## Variation 3 

[Functional] The user shall input a four-ball color sequence to determine the order in which the application should detect and knock out balls. 

[Non-Functional] The car shall remain within the boundary course and cannot utilize the line-tracking feature for finding the balls. 

[Non-Functional] The application shall detect (i.e., find) balls, one at a time, in the order provided.  The car shall perform the following activities once a ball is detected: 

[Functional] Change vehicle LEDs to match the color of the detected ball 

[Functional] Drive the car into a ball to knock the ball outside the boundary.  If the ball remains inside the border, the application should continue attempting to knock the ball outside of the border until a boundary wall is detected 

[Non-Functional] Flash LEDs indicate the condition has been met before transitioning to the next ball in sequence.  LEDs should reset to off after three seconds.

[Functional] This is repeated until all four balls have been removed from the course. 

## Variation 4

[Functional] Create a three-class YOLO object model.  

[Non-Functional] (Sample size should be around 150-200 images taken in various backgrounds and angles per object.  The complexity of the chosen object will determine the sample size.) 

[Non-Functional] The car shall stay within the provided boundary course and cannot utilize the line-tracking feature for finding the balls.

[Functional] The car shall avoid objects within the provided boundary course. 

[Functional] The car shall detect the objects found in its object model.  Upon detecting an object the following should occur:

- [Functional] Flash LEDs in a pattern indicating the object found 

- [Functional] Drive towards the detected object and stop between one to two feet away from the object 

- [Non-Functional] Flash LEDs indicating movement toward the object has been completed 

- [Non-Functional] Pause the car for five seconds before continuing to the next object 

- [Functional] The application completes once all objects are detected and object detection steps are completed.

# Constraints:
Must work in Python on a Raspberry Pi platform. Must also use A.I. to scan images and machine learning necessary to detect balls within its boundaries.
Must have proper equipment to set up course for the car.

# Stakeholders:

## Users:
### Mercer staff
Staff, like professors or maintenance, should be able to use our product. Mercer staff would be looking for more details and testing the extent of A.I. image recognition system, so they should be considered tech savvy. We should expect them to be critical of the system and be able to give substantial feedback on our product, ranging from code to quality control.

### Mercer students
Students at Mercer are also very good at using technology and adapting to new products. They would be a very good type of user to test the product on and interview, however, we should not expect them to be as critical as professors may be simply because of a lack of experience.
Possible guests
This is a category of people in-between students and staff. They will most likely be not tech savvy and therefore even more casual at using our product than students.

## Acquirer:
### Mercer University
After the project’s completion, our product’s name will be under Mercer University. The University will want our project to be working, they don’t care about its intricacies.

## Producer:
### Freenova Robot Team 2
As Freenova Robot Team 2, we will be producing this product and maintaining it through our vision.

## Regulator:
### Dr. Allen & Professor Munday
Dr. Allen provided us with the project proposal, Professor Munday will be overseeing our project.
