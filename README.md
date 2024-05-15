# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: Get the built-in module in pyhton called robomaster and import the robot then import camera
from the same module, And also import time for time intervals.


Step2: Initialise the robot by giving initialize function for the robot to get commands from the user and move


Step3: Assign a value to the x axis so that the robot moves in the forward direction and for the robot to
move towards left or right give a certain value to y axis and for turning toward left and right assign
the value of degrees in the z axis.

Step4: At the same time also assign the speed of xy movement speed of all the x and y.

Step5: The function set_led would determine the colors of the led lights on every four sides of the robot
by certain values of rgb to be given for getting various colors to be displayed in the robot.

Step6: After giving a lot of commands for the robot to move in a certian path with colors give it some time
for the robot to rest and then close the robot.

Step7: After giving a lot of commands for the robot to move in a certian path with colors give it some time
for the robot to rest and then close the robot.


## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")
 ep_chassis = ep_robot.chassis
ep_led = ep_robot.led
ep_camera = ep_robot.camera
print("Video streaming started.....")
ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
ep_chassis.move(x=2.45, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
ep_chassis.move(x=0.5, y=0, z=80, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
ep_chassis.move(x=1, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")
ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")
ep_chassis.move(x=0, y=0, z=-120, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")
ep_chassis.move(x=-1.5, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")
ep_chassis.move(x=0, y=0, z=-43, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")
ep_chassis.move(x=0, y=1.4, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")
ep_chassis.move(x=2.05, y=0, z=0, xy_speed=1.3).wait_for_completed()
ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")
ep_chassis.move(x=0, y=0, z=82, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")
ep_chassis.move(x=0.55, y=0, z=0, xy_speed=1.3).wait_for_completed()
ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")
ep_chassis.move(x=0, y=0, z=0, xy_speed=1.3).wait_for_completed()
ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")
time.sleep(4)
ep_camera.stop_video_stream()
print("Stopped video streaming.....")
ep_robot.close()
```
## MobileRobot Movement Image:

Insert image here
![image](https://github.com/Sharonsteffani2005/mobilerobot-openloopcontrol/assets/144979934/10b8c91f-c058-432f-86df-467795d5377b)

![image](https://github.com/Sharonsteffani2005/mobilerobot-openloopcontrol/assets/144979934/ea4c5a55-fe6b-40b1-9076-771c534b3e23)


## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here https://youtu.be/OH3qJImNaX8


## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


