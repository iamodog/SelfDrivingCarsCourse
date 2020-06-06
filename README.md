# SelfDrivingCarsCourse

## PARTIE 1 JORAN

## PARTIE 2 JORAN

## Visual Perception for Self-Driving Cars

The goal of the perception stack is to provide the motion planning stack enough
information about the driving environment so that the latter can achieve its
mission in a safe and efficient way.

The perception task is (in a way) already solved. We know how to do object
recognition, classification, segmentation, even monocular depth estimation. We
can do instance segmentation and track dynamic objects as long as they're 
covered by camera/LIDAR. The only remaining question is what does the motion
planner needs ? 

This however is still an area of active research. We could look at it in 2
different ways:
  1. End-to-end solution, the vision stack outputs the behavior.
  1. Output as much info as possible from the vision stack, then find a way to
     solve motion planning.

In this part, we'll talk about the second solution. Let's assume, for the sake
of simplicity, that we need to know 3 things to drive car:
  1. We need to know where should we drive, i.e. road and lane lines
  1. We should know the position of the other agents (cars, pedestrains, etc.)
     in the same environment, so that we can drive without colliding.
  1. We have to be aware of the regulatory elements in our driving
     environment (stop signs, crosswalks, etc.)

All of this can be achieved just with an RGB camera input, with just 3
deep learning models.

### Segmentation
Image segmentation is the process of classifying every pixel of an image into
a given set of labels. In this case, we can think of different types of labels:
dynamic object, road, regulatory element, etc.

[segmentation](./imgs/segmentation.jpeg)

### Object Recognition

### Depth Estimation

### Putting it all together

## Motion Planning for Self-Driving Cars

