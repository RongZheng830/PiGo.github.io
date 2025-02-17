![Image](https://github.com/user-attachments/assets/94fb9202-74d2-49bc-ae0d-d3c7552f86f0)))

# Week 1

## Step-by-Step Assembly
   First, secure the Raspberry Pi board to the base using screws and double-headed standoffs. Then, attach the adapter board to the Raspberry Pi with screws.

   Align the module that can drive the speaker to the corresponding interface on the Raspberry Pi board. Then, mount it onto the base using screws and standoffs. The standoffs used here are slightly taller than those of the Raspberry Pi.

  Align the plastic disc with the standoffs and secure it using screws. Connect the speaker’s interface to the output terminal of the driver module and install it. Finally, use glue to attach the disc and the speaker.

  The obstacle avoidance module should be installed at the front of the car’s base. Secure it using shorter standoffs and screws. After connecting the voltage detection module to the voltmeter, secure it to the base using screws.

First, install the two 2-DOF (two-degree-of-freedom) servo platforms onto the chassis. The servo shafts should not be positioned at the center but rather placed on both sides of the car, closer to the USB interface of the module. A 2-DOF platform means it can move in two directions. First, the servo horn can freely rotate 90 degrees to both sides. After mounting the servos, a bracket with servo horns on both sides needs to be installed, allowing movement in the vertical direction. Finally, mount the camera onto the platform.

During the assembly, we failed to connected all the wires successfully because we tied the battery to the wrong place with plastic cable ties. Besides, we did not install the wheels for the reason that either we lost the wheels or the seller forgot to deliver. These problems limited us to go further in this project during the lab time.
## Problems encountered 
### Problem 1 : install the caster wheel
  When the materials were delivered, it was discovered that the caster wheel was missing. By analyzing the connected shaft, the model of the coupling and the wheel was determined. After Assembly, it was found that the coupling of the selected TT motor was too long, so its length was shortened to fit the wheel.
### Problem 2 : replace with a longer zip tie
  During assembly, it was found that the purchased zip ties were too short. Some couldn’t be fastened due to space occupied by other components, so longer zip ties were purchased. (2.5*200mm)

![Image](https://github.com/user-attachments/assets/2113eac6-39a3-461f-8f79-90a258779228)

![Image](https://github.com/user-attachments/assets/170ca9c8-4256-494b-b975-f715867c8bc7)

# Week 2
## Handle the issue with week1
### Problem 1 :  to prevent movement issue
If the coupling of a regular tire is ground unevenly, the movement of the small vehicle will be affected. However, this issue does not occur when using Mecanum wheels. The wheels were successfully installed. During the final test, one wheel was found to be slightly loose.

![Image](https://github.com/user-attachments/assets/e7877508-a7ca-456c-b919-a7c7dc40d365)

### Problem 2 : make battery removal easier
Using zip ties instead of glue to secure the battery can prevent situations where wiring errors make battery removal impossible, as some wires are located on the back of the battery. After removing the previously zip ties which are tangled complicatedly, the battery was secured with a simpler binding method.

## Burn raspberry Pi OS to an SD Card
 Download and install Raspberry Pi Imager. Then Insert the SD card. After selecting SD card and  Operating System, Burning can be stared. Wait for the writing process to complete, and the Imager will automatically eject the SD card. After Burning is complete, it is required to configure WiFi, SSH and  language...
 
### Create  a virtual environment 
Activate the virtual environment matters a lot. Before configuring WiFi, SSH and  language, a virtual environment should be created.

### Connect WiFi
Found that wireless connection to the school's campus network was not possible. 

# Week 3
## Import the test code for motion
 We successfully resolved the network connection issue. Now we can test the code for the car's operation.
https://github.com/user-attachments/assets/11ad9070-86e4-4351-91ab-22c2cbb3d37e
Therefore, we have confirmed that the car and the code can function properly.
## OpenCV
The computer vision part is based on OpenCV for target recognition and path tracking. The camera can capture real-time images of the environment. After that, through the color space conversion, identify the target color and Canny algorithm to identify the path or obstacle contour, match the contour detection with the shape to achieve the identification and tracking of specific targets. Next, the algorithm is used to lock the target and adjust the direction of travel of the trolley according to the target position to realize autonomous tracking. Finally, by detecting the road edge line through the Hough transform and combining with the PID control algorithm, the trajectory of the McNamee wheel is adjusted to stabilize the trolley along the predetermined path.
##  Face Recognition and Visual Cruise Performance Test 
Lifting the camera up and pointing it at the group's face, an inspection of the program's runtime screen revealed that accurate face recognition was indeed available. The car stopped running when a face was recognized.

![Image](https://github.com/user-attachments/assets/1e710760-4593-4bf8-a752-5277a49673dd)