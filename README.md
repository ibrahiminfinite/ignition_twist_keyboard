# ignition_twist_keyboard
Modified version of  https://github.com/ros-teleop/teleop_twist_keyboard
The ROS publish features has been replaced with the ignition transport publish so that this keyboard can directly be used with ignition
This keyboard has additional key bindings (y /h) to control robot height as this keyboard will be used for a legged robot testing for my purposes
Additionally the Z linear velocity is hardcoded to zero, be sure to change it if using with Aerial vehicles.

## Features

This particular implementation does away with keeping the history of previous speed settings, and heavily cuts down on the amount of printing that is done to the terminal via the use of carriage returns (\r).

Furthermore, the last command that was sent is reflected, and invalid commands are identified as such.


## Usage

Same as the original

```
Reading from the keyboard  and Publishing to Twist!
---------------------------
Moving around:
   u    i    o
   j    k    l
   m    ,    .

For Holonomic mode (strafing), hold down the shift key:
---------------------------
   U    I    O
   J    K    L
   M    <    >

t : up (+z)
b : down (-z)

y : increase robot height by 0.025m
h : decrease robot height by 0.025m


anything else : stop

q/z : increase/decrease max speeds by 10%
w/x : increase/decrease only linear speed by 10%
e/c : increase/decrease only angular speed by 10%

CTRL-C to quit
```

