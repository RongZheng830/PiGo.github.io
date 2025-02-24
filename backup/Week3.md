# Week 3
## Import the test code for motion
 We successfully resolved the network connection issue. Now we can test the code for the car's operation.
https://github.com/user-attachments/assets/11ad9070-86e4-4351-91ab-22c2cbb3d37e
Therefore, we have confirmed that the car and the code can function properly.
## OpenCV
The computer vision part is based on OpenCV for target recognition and path tracking. The camera can capture real-time images of the environment. After that, through the color space conversion, identify the target color and Canny algorithm to identify the path or obstacle contour, match the contour detection with the shape to achieve the identification and tracking of specific targets. Next, the algorithm is used to lock the target and adjust the direction of travel of the trolley according to the target position to realize autonomous tracking. Finally, by detecting the road edge line through the Hough transform and combining with the PID control algorithm, the trajectory of the McNamee wheel is adjusted to stabilize the trolley along the predetermined path.
##  Face Recognition 
Lifting the camera up and pointing it at the group's face, an inspection of the program's runtime screen revealed that accurate face recognition was indeed available. The car stopped running when a face was recognized.

![Image](https://github.com/user-attachments/assets/1e710760-4593-4bf8-a752-5277a49673dd)