# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
Step1:
Use from robomaster import robot
Step2:
Choose the x,y,z axis movement distance(meters)
Step3:
Give ep_chassis.move to move straight.
Step4:
Give time.sleep() for a break 
Step5:
Give ep_chassis.drive_speed to have a circular movement.
## Program
Developed by:Yamuna M
Register Number:212223230248
```python
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0.4, y=0, z=67,xy_speed=1.1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=204,b=255,effect="on")

    ep_chassis.move(x=0.85, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=0,effect="on")

    ep_chassis.move(x=0, y=-1.4, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
    

    ep_chassis.move(x=0, y=0, z=102).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")
    
    ep_chassis.move(x=0.6, y=0, z=-30, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=255,effect="on")
    
    ep_chassis.move(x=1.1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
     
    ep_chassis.move(x=0, y=0, z=130).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x=0, y=1.55, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=10).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=153,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=153,b=0,effect="on")

    ep_chassis.move(x=0, y=-0.6, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")

   

    ep_chassis.move(x=0, y=0, z=0,xy_speed=1.3 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:
![image](https://github.com/yamunadass/mobilerobot-openloopcontrol/assets/138971172/d13ab5a3-944e-4ad4-b82b-3a3b78b5b580)
![image](https://github.com/yamunadass/mobilerobot-openloopcontrol/assets/138971172/16ba57e3-d6a6-4dec-baf9-f3847c047e34)
## MobileRobot Movement Video:
https://youtu.be/KJreAHr7dZk?feature=shared
## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.
```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
