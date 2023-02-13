# Path-Planning-ROSbot

## 1. Create a separate workspace and clone the package by running each command individually on the terminal
```
mkdir -p ~/path_plan/src/
cd ~/path_plan/src
git clone https://github.com/sabrinamkb/Path-Planning-ROSbot.git
cd ..
catkin_make 
source devel/setup.bash
```

## 2. Open a terminal and launch the RPLiDAR (DO NOT CLOSE THIS TERMINAL, KEEP IT RUNNING IN THE BACKGROUND)
```
cd ~/path_plan/src/tutorial_pkg
rosrun rplidar_ros rplidarNode
```

## 3. On another terminal, run the following commands:(DO NOT CLOSE THIS TERMINAL, KEEP IT RUNNING IN THE BACKGROUND)
```
cd ~/path_plan/src/tutorial_pkg
roslaunch rosbot_ekf rosserial_bridge.launch serial_port:=/dev/ttyS4 serial_baudrate:=460800
```

## 4. On another terminal, run the following commands: (DO NOT CLOSE THIS TERMINAL, KEEP IT RUNNING IN THE BACKGROUND)
```
cd ~/path_plan/src/tutorial_pkg
rosrun tutorial_pkg drive_controller_node
```

## 5. On another terminal, run the following commands: (DO NOT CLOSE THIS TERMINAL, KEEP IT RUNNING IN THE BACKGROUND)
```
cd ~/path_plan/src/tutorial_pkg
rosrun tf static_transform_publisher 0 0 0.1 3.14 0 0 base_link laser 100
```

## 6. On another terminal, run the following commands: (DO NOT CLOSE THIS TERMINAL, KEEP IT RUNNING IN THE BACKGROUND)
```
cd ~/path_plan/src/tutorial_pkg
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

## 7. On another terminal, run the following commands: (DO NOT CLOSE THIS TERMINAL, KEEP IT RUNNING IN THE BACKGROUND)
```
cd ~/path_plan/src/tutorial_pkg
rviz
```

