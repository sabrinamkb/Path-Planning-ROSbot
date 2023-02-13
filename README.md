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

## 2. Open a terminal and run the following command
```
roslaunch rosbot_ekf all.launch rosbot_pro:=true
```

## 3. Open a separate terminal and run the following
```
cd ~/path_plan/src/tutorial_pkg
roslaunch tutorial_pkg maze_world.launch
```

## 3. Set up your rviz
a. In rviz add Tf and /scan, then add /map by selecting "By Topic." At the beginning there could be no map, you may need to wait few second until it is generated.
b. Now drive your robot around and observe as new parts of map are added, continue until it moves around the whole track.

## 4. Save the map
```
roscd tutorial_pkg
mkdir maps
cd maps
rosrun map_server map_saver -f maze_map
```

## 5. Final launch
```
cd ~/path_plan/src/tutorial_pkg
roslaunch tutorial_pkg tutorial_9.launch 
```

## 6. Open another terminal to run rviz
```
rviz
```

## 7. Set your target
a. You should be able to set your target point on the track using 2D Nav Goal and robot should drive there
